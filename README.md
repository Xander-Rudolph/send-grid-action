# send-grid-action

## example usage:
```
name: Send Email

on: [workflow_dispatch]

jobs:
  send-email:
    runs-on: ubuntu-latest
    steps:
      - name: Send email using SendGrid
        uses: xander-rudolph/send-grid-action@main
        env: 
          sendGridApiKey: ${{ secrets.SENDGRID_KEY }}
        with:
          toEmail: addressee@example.com
          fromEmail: emailaddress-registered-to-sendgrid@example.com
          subject: "This is an email subject"
          body: "This is an email from github actions"
```
