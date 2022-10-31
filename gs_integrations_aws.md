---
layout: default
title: Enabling AWS Integration
parent: Enabling Integrations
nav_order: 1
---
# AWS Integration

Kubiya offers an easy-to-use integration with Amazon Web Services. This integration allows you to perform a variety of actions on AWS using Kubiya.

To complete the AWS Integration you will need to create a Role for Kubiya using the Kubiya AWS account number and enable the integration at the Kubiya CLI.

## Create a Role in AWS

1. Login to your AWS console and navigate to the Identity and Access Management (IAM) page.
2. Click on the 'Roles' section
3. Click "Create Role" button in the top right corner

<img src="images/roles.png">

4. In the "Select trusted entity" dialog:
    1. Select "AWS account"
    2. Select "Another AWS account
    3. Enter the Kubiya Account ID in the identifier input box
            564407622114
    4. Click Next

<img src="images/trusted-entities.png">

5. In the 'Policies' dialog, select the access rules that you would like Kubiya to have access to, then click Next

<img src="images/policies.png">

6. In the "Role details" dialog:
    1. Name the role, you will need this later.
    2. Confirm the Kubiya Account ID in the JSON under "Step 1: Select trusted entities"
    3. Confirm the selected permissions under "Step 2: Add permissions"
    4. If correct, click the "Create role" button

<img src="images/confirmation.png">




