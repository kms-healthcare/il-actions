# Google Chat Notification for GitHub Actions

> [!IMPORTANT]
> This javascript action is a cloned version of [Google Chat Notification](https://github.com/Co-qn/google-chat-notification) because the original repository is not maintained anymore and have a risk of being deleted. It's also good already, so we just need to get a lite copy of built file and use it internally.

## Usage
### Parameters
|Name|Required|Description|
|:---:|:---:|:---|
|name|true|Job name. Used for notification titles.|
|url|true|Google Chat Webhook URL.|
|status|true|Job status. Available values are `success`, `failure`, `cancelled`. We recommend using `${{ job.status }}`|

### Example
```yaml
      - name: Google Chat Notification
        uses: kms-healthcare/il-actions/ggchat-github-report@main
        with:
          name: "Test Workflow - Google Chat Notification"
          url: ${{ secrets.GOOGLE_CHAT_WEBHOOK_URL }}
          status: ${{ needs.example-success-job.result }}
        if: always()
```
