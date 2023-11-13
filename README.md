# dance-standard-pipelines

These pipelines are in standard tekton format. They can be found in ./pac/pipelines and ./pac/tasks

# Install 

1. To use these pipelnes, copy the appropriate build from ./pac into .tekton 
    - docker-build uses dockerfiles to build your app
    - nodejs-build node - npm based build for node.js 
    - java-build -  s2i-java builder 

2. Modify the copied files using the placeholders names in template format for the specifics for your application

   - `{{values.appName}}`  the app name for your component 
   - `{{values.dockerfileLocation}}`  the dockerfile location for your component
   - `{{values.namespace}}`  the namespace location for your component
   - `{{values.image}}`  the image for your destination 
   - `{{values.namespace}}`  the namespace location for your component
   - `{{values.buildContext}}`  the namespace location for your component
    

## Backstage
Modify the template placeholders to match your backstage template vars  
Note, PaC also has `{{variables}}` and you should not modify those. 

   - `{{values.appName}} -> ${{ values.appName }}`   
   - `{{values.dockerfileLocation}}-> ${{ values.dockerfileLocation }} `  
   - `{{values.namespace}}-> ${{ values.namespace }} ` 
   - `{{values.image}}-> ${{ values.image }} ` 
   - `{{values.namespace}}-> ${{ values.namespace }} ` 
   - `{{values.buildContext}}-> ${{ values.buildContext }} `   

 TBD use backstage format ?