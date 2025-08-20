---
title: "MCP - Model Context Protocol"
ring: trial
segment: architecture-pattern
tags: [protocol]
---

The Model Context Protocol (MCP) is an open protocol that standardizes how applications provide context to LLMs. Think of it as a "USB-C port for AI applications" - providing a standardized way to connect AI models to different data sources and tools.

The protocol was introduced by Anthropic in november 2024. The specification and developer tools are opensourced [here](https://github.com/modelcontextprotocol)

## Key Features and benefits

- **Standardized Integration**: Unified protocol for connecting LLMs to various tools and data sources
- **Reusable MCP Servers**: Pre-built server implementations for common use cases
- **Modular Architecture**: By composing AI applications with MCP servers you are able to build flexible and reusable architectures
- **Security**: Built-in security patterns
- **Real-time Updates**: Event-driven architecture

## Technical Details

MCP follows a client-server architecture where a host application (with MCP Client(s)) can connect to multiple servers (=MCP Server). MCP Server can be local or remote. The connection is opened by the client - as long as it is required.

The transport layer can be Stdio (for local) or HTTP with SSE (Server-Sent Events) (for local or remote). Data is exchanged in JSON-RPC protocol.

### Architecture

MCP follows a client-server model with:

- **MCP Hosts**: Programs like Claude Desktop, IDEs, or AI tools
- **MCP Clients**: Protocol clients maintaining 1:1 server connections
- **MCP Servers**: Lightweight programs exposing specific capabilities
- **Data Sources**: Local files, databases, and remote services

## MCP Server Capabilities

1. **Resources**: File-like data with discovery and read operations
   - Server expose a discovery endpoints via `resources/list` and `resources/templates/list`. The only difference is that the latter one contains uri to ressources in a template format (using [RFC6570]https://www.rfc-editor.org/rfc/rfc6570.html))
   - To read resources, the client must use `resources/read` endpoint
   - To get notifications about changes, the client must use `resources/subscribe` endpoint
2. **Prompts**: Reusable templates with structured formats
   - Server can discover prompts via `prompts/list` endpoint. Prompt support argument definitions
   - To get a Prompt the Client requests `prompts/get` endpoint (optional with arguments). They get back a list of "messages" with description and conteactxt that can be used as LLM input.
3. **Tools**: Action execution with approval flows
   - Discovery: Clients can list available tools through the `tools/list` endpoint
   - Invocation: Tools are called using the `tools/call` endpoint, where servers perform the requested operation and return results. The result can be of type Text, Image, Audio or EmbeddedRessource.
4. **Notifications**: Real-time updates and subscriptions

### Tools discovery

The most used feature of MCP is, to discover and use tools. 
This gives the client access to possibly any action, that aMCP server exposes.

Tools are exposed with the following data structure:

```json
{
  name: string;          // Unique identifier for the tool
  description?: string;  // Human-readable description
  inputSchema: {         // JSON Schema for the tool's parameters
    type: "object",
    properties: { ... }  // Tool-specific parameters
  },
  annotations?: {        // Optional hints about tool behavior
    title?: string;      // Human-readable title for the tool
    readOnlyHint?: boolean;    // If true, the tool does not modify its environment
    destructiveHint?: boolean; // If true, the tool may perform destructive updates
    idempotentHint?: boolean;  // If true, repeated calls with same args have no additional effect
    openWorldHint?: boolean;   // If true, tool interacts with external entities
  }
}
```

Once the endpoint of an MCP server is know, it is very simple to use it from within a client:

```python
from mcp import Client

client = Client()
client.connect("document-processor")
result = client.tools.call("process_document", {"file_path": "doc.pdf"})
```

### MCP Client features

The MCP Client runs on the "host" and they are responsible for establishing and managing connections with MCP servers. Client can also offer endpoints that the server can use:

- _Roots_: Roots allow servers to ask for specific directories or files to operate on.
- _Sampling_: allows servers to request LLM completions through the client. This makes sure that servers can use the LLM features on the host, and therefore maintain data privacy.

## Security Concepts

- Use TLS and Authentication & Authorization with proper access control (e.g. OAuth and RBAC).
- The proposed way to secure MCP is OAuth (MCP Servers are OAuth 2.0 Protected Resources). This way the security concept can follow "Zero Trust" and existing SSO solutions can be used.
- Input Validation: Strict schema validation to prevent injection and malformed requests.

## Example Usage

A popular MCP Client is Claude desktop, where users can specify the available MCP Servers in a configuration file. E.g. the following configuration makes MCP Servers for filesystem and browseraccess available:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/Users/username/Documents"
      ]
    },
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    }
  }
}
```

There is also a couple of Inspectors available, like [MCP Inspector](https://github.com/modelcontextprotocol/inspector), that can be used to inspect MCP servers:

![MCP inspector](/images/mcp-inspector.png)

## Design Effective MCP Interfaces: Every MCP Tool Response as a Prompt

Effective Model Context Protocol (MCP) design goes beyond simply exposing API endpoints. Each tool response should be viewed as an opportunity to guide and inform the model’s reasoning process.

Key principles for designing MCP tools include:

- **Think in Prompts, Not Just APIs:**  
  AI models interpret tool specifications as text prompts rather than understanding endpoints in the way humans do. The clarity and quality of these prompts directly influence model behavior.

- **Design for Intent, Not Infrastructure:**  
  Avoid mapping tools directly to backend functions. Instead, abstract high-level user intentions (for example, “summarize user activity”) rather than exposing only low-level operations.

- **Tool Responses Should Guide the Model:**  
  Each tool response should provide information that helps the model determine its next steps. The goal is not just to return data, but to support the model’s reasoning and decision-making.

- **Use Structure Sparingly:**  
  Overly complex, deeply structured arguments can hinder model performance. Favor simpler, prompt-aligned interfaces that are easier for models to interpret and use effectively.

## References and Links

- [Official MCP Spec](https://github.com/model-context-protocol/spec)
- [Website with a list of MCP Servers](https://mcpservers.org/) [Awesome MCP Servers List](https://github.com/punkpeye/awesome-mcp-servers)

## Related:

- Related: [RAG](/architecture-pattern/rag/), [GraphRAG](/architecture-pattern/graph_rag/)
