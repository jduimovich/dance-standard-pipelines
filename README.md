# dance-standard-pipelines

These pipelines are in standard tekton format. They can be found in ./pac/pipelines and ./pac/tasks

# Install 

1. To use these pipelnes, copy the appropriate build from ./pac into .tekton 
    - docker-build uses dockerfiles to build your app
    - nodejs-build node - npm based build for node.js 
    - java-build -  s2i-java builder 

2. Modify the copied files for your application
   - `{{values.appName}}`  the app name for your component 
   - `{{values.dockerfileLocation}}`  the dockerfile location for your component
   - `{{values.namespace}}`  the namespace location for your component