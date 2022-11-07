---
layout: default
title: Actions
parent: Key Concepts
nav_order: 2
---
# What are Actions?
Actions allow you to perform a specific task. For example, you can use an action to get a list of all the issues in a JIRA project, or to create a new issue in JIRA.

Individual Actions that are related to each other are grouped in Action Stores.  For example, the JIRA action catalog contains all the actions that are related to JIRA.

## Action Stores
Action stores are built using the Kubiya SDK and are available to all users of the platform using a source control based approach.

Action Stores are compiled Docker containers that expose a REST API that Kubiya can call to perform the actions defined within the store.  Kubiya uses an on-demand, serverless approach to Action Stores and will launch the container upon request of a specified action.  The Action Store will be allowed to run for a short period of time, in case an additional action from the store is required, before the container is terminated.

Kubiya treats action stores as a black box. The contents of the actual store are irrelevant and Kubiya will only interact with the exposed REST API.

Action Stores are built, published and managed from the Kubiya CLI.

⏭️ Next: [Key Concepts -> Integrations](kc_integrations.html)