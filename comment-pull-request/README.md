# Comment Pull Request Composite Action

> [!NOTE]
> This composite action allows you to automatically comment on a pull request in your GitHub repository.

## Usage

To use this action, you need to include it in your workflow file. Here's an example of how to do it:

### Single-line comment
```yaml
- name: Comment Pull Request
  uses: kms-healthcare/il-actions/comment-pull-request@main
  with:
    message: 'Hello, world!'
    github-token: ${{ secrets.GITHUB_TOKEN }} # Optional, default is github-actions bot token
```

### Multi-line comment

```yaml
- name: Comment Pull Request
  uses: kms-healthcare/il-actions/comment-pull-request@main
  with:
    message: |
      # Hello, world!
      This is a multi-line comment.
```

Message is required. GITHUB_TOKEN is optional. If you don't provide it, the action will use the github-actions bot token.

> [!NOTE]
> Message should be in markdown format.