# Build and Push Docker Image to Google Cloud Container Registry

## Usage

To use this composite action, include it in your workflow file. Here's an example of how to do it:

```yaml
- name: Build and Push Docker Image to Google Cloud Container Registry
  uses: kms-healthcare/il-actions/gcr-build-push@main
  with:
    image-name: 'your-docker-repo/image-name'
    image-tag: 'your-docker-image-tag'
    gcloud-registry: 'your-gcr-registry'
    gcloud-project-id: 'your-gcp-project-id'
    gcloud-secrets: 'your-gcp-service-account-json-key'
```

For optional inputs, you can follow the inputs in the action.yml file.