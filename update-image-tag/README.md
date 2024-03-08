# GitOps - Update K8S Manifests

## Usage

To use this composite action, include it in your workflow file. Here's an example of how to do it:

```yaml
- name: Update K8S Manifests
  uses: kms-healthcare/il-actions/update-image-tag@main
  with:
    repo: "repo name contains the k8s manifests"
    github-token: "token used to commit the manifests commit"
    values-file: "values file k8s"
    xpath: "image xpath"
    tag: "new image tag"
```

For optional inputs, you can follow the inputs in the action.yml file.