---
layout: default
title: Enabling Integrations
parent: Getting Started
nav_order: 3
has_children: true
---
# Enabling Integrations from the CLI

Integrating Kubiya with other applications provides extended functionality allows the workflows to interact with the outside world.  For instance, given a certain event or approval that is required, you may want to open a ticket in Jira.  Kubiya supports Integrations with Slack, Jira, AWS and several identity providers.

## Slack Integration

Slack Integration is available through <a href="https://slack.com/oauth/v2/authorize?client_id=2154513364934.2307890902273&scope=app_mentions:read,channels:manage,chat:write,conversations.connect:write,files:write,groups:read,groups:write,im:history,im:write,mpim:history,mpim:write,pins:write,reactions:read,reactions:write,usergroups:read,users:read,users:read.email,team:read,users.profile:read,channels:read,im:read&user_scope="><img alt="Add to Slack" height="20" width="70" src="https://platform.slack-edge.com/img/add_to_slack.png" srcSet="https://platform.slack-edge.com/img/add_to_slack.png 1x, https://platform.slack-edge.com/img/add_to_slack@2x.png 2x" /></a>

By Clicking on the Add to Slack button above you will be prompted to approve Kubiya's access to your workspace.

<img src="images/add-to-slack.png" height="300" width="250">

If successful, Slack will return the following:

<img src="images/add-success.png">

## Jira Integration

## AWS Integration

Kubiya offers an easy-to-use integration with Amazon Web Services. This integration allows you to perform a variety of actions on AWS using Kubiya.

To complete the AWS Integration you will need to create a Role for Kubiya using the Kubiya AWS account number and enable the integration at the Kubiya CLI.

Complete instructions can be found [here](gs_integrations_aws.html).


