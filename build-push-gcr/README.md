# Build and Push Docker Image to Google Cloud Container Registry

> [!NOTE]
> This readme provides instructions for using the composite action to build and push a Docker image to Google Cloud Container Registry.

## Usage

To use this composite action, include it in your workflow file. Here's an example of how to do it:

```yaml
- name: Build and Push Docker Image to Google Cloud Container Registry
  uses: kms-healthcare/il-actions/build-push-gcr@main
  with:
    docker_image_name: 'your-docker-repo/image-name'
    docker_image_tag: 'your-docker-image-tag'
    gcloud_registry: 'your-gcr-registry'
    gcloud_project: 'your-gcp-project-id'
    gcloud_service_account_key: 'your-gcp-service-account-json-key'
```

For optional inputs, you can follow the inputs in the action.yml file.