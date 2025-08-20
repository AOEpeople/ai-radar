# AOE Technology Radar AI - Content


This is the location of AOE AI Radar 

published under: https://ai-radar.aoe.com/

If you want to build your own techradar you may want to have a look at https://github.com/AOEpeople/aoe_technology_radar instead.

## Content Guidelines

New blips should be tagged. The following tags are currently established:

>Todo: Reduce number of tags!
    
* UI
* automation
* chat
* extraction
* benchmarking
* evaluation
* knowledge
* patterns
* platform
* prompting
* protocol
* retrieval
* extraction
* security
* workflow
* sovereignty
* observability
* vector-db
* model-serving
* protocol

e.g. use like this:

```md
tags: [tools, prompts]
```

## Development

### Build the radar
```
npm i
npm run serve
```

Then open here: http://localhost:3000/techradar

### Build the radar with static files
```
npm i
npm run build
```

### GitLab Pages Deployment

To deploy the radar on GitLab Pages, the included `.gitlab-ci.yml` will automatically:
   - Build the project using Node.js
   - Deploy it to GitLab Pages
   - The site will be available at your GitLab Pages URL after the pipeline completes

Note: The deployment will happen automatically when you push to the `main` branch.
