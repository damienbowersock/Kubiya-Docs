---
layout: default
title: Actions
parent: Key Concepts
nav_order: 2
---
# What are Actions?
Actions allow you to perform a specific task. For example, you can use an action to get a list of all the issues in a JIRA project, or to create a new issue in JIRA.

Actions are created as part of action stores. Action stores are a collection of actions that are grouped together. For example, the JIRA action catalog contains all the actions that are related to JIRA.

## Action Stores
Action stores are built using the Kubiya SDK and are available to all users of the platform using a source control based approach.

Essentially, action stores are simple Docker images which exposes a set of actions. The actions are exposed as a REST API which is used by Kubiya to execute the actions.

Kubiya treats action stores as a black box. It does not care about the implementation of the actions, it only cares about the REST API that is exposed by the action catalog.

You can use the Kubiya CLI to build and publish action stores. You can also use the Kubiya CLI to manage the action stores that are available to your users.

Kubiya uses a serverless approach to execute actions. This means that the actions are executed in a container which is created on demand. The container is destroyed once the action has been executed. but it is not destroyed immediately. Instead, the container is kept alive for a short period of time to allow for reuse.