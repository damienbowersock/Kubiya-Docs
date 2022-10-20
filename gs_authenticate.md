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

    kubiya auth --token <your_operator_key>

The CLI should open the browser and prompt you to authenticate using your organization’s authentication method:

<img src="https://kubiya-static-objects.s3.amazonaws.com/kubiya_enter_org_details.png" width="350" height="475" />

1. Enter the organization name and click on the “Continue” button. The organization name is received from Kubiya upon registration
2. Log in with the identity provider
3. Authentication complete, you can now access the Kubiya CLI.

## Test your authenticated session

Run the following command in your terminal to validate that your session is truly authenticated:

    kubiya auth validate
You should see a validation message:

    ✅ Authenticated to *your organization name* as *your_user_name*

⏭️ Next: Setting up an integration