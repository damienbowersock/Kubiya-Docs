---
layout: default
title: Authenticating Kubiya from the CLI
parent: Getting Started
nav_order: 2
---
# Authenticating Kubiya from the CLI

In order to use the Kubiya CLI you need to authenticate your account. Authentication requires the following:

* Access to your organization authentication method (such as Google, or Okta)
* Your Kubiya operator key - which will allow you to operate Kubiya from the CLI

## Authentication
In order to authenticate, run the following command in your terminal:

    kubiya auth -t <your_operator_key>

The CLI should open the browser and prompt you to authenticate using your organization’s authentication method:

<img src="https://kubiya-static-objects.s3.amazonaws.com/kubiya_enter_org_details.png" width="350" height="475" />

1. Enter the organization name and click on the “Continue” button. The organization name is received from Kubiya upon registration
2. Log in with the identity provider
3. Authentication complete, you can now access the Kubiya CLI.

## Test your authenticated session

To test your authentication return to Slack and click on the Kubiya App Icon

<img src="images/kubiya-icon.png>

Send a 'hello' message to the Kubiya App.  If your authentication was successful, you will recieve the following response from the app:

<img src="images/hello-response.png>

⏭️ Next: [Setting up an integration](gs_enable_integrations.html)