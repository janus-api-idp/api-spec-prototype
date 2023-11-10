# API Spec prototype

This is a Tekton pipeline to run Spectral on specific API guidelines. You'll need to create a custom Docker image for your Spectral task (https://github.com/janus-api-idp/spectral-image).

## Bootstrapping

To trigger the pipeline, you need to apply configs for both spectral-task.yaml and microcks-import-task.yaml, then create the pipeline

   `oc apply -f .tekton/pipeline`

Now, if the API specification passes the Spectral rule, the pipeline will succeed. If not, it will fail, and you can check the Spectral report for details on the issues.
