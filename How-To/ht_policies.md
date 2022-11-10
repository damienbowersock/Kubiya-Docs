---
layout: default
title: Policies
parent: How To Guides
has_children: true
nav_order: 2
---

# Policy How-To Guide

## What are Policies

By default, Kubiya implements a "zero-trust" strategy regarding access to workflows by users.  Therefore, a policy must be established to allow a given user access to a given workflow.

## Create a Policy

To create a policy, we must associate a set of allowable actions with a user's login email.  This can be done at the Kubiya CLI using:

```bash
kubiya policy create --policy-name <policy name> 
    --action-ids <comma-seperated list of allowed actions>
    --workflow-ids <comma-serperated list of allowed workflows>
    --allowed-entity <user login email>
```

### Available Action IDs

Kubiya supports allowing users to access the following functions:

- policy.create - create a new policy
- policy.delete - delete an existing policy
- user.invite - Invite new users to Kubiya
- permissions.approve - Approve access permissions
- workflow.run - Run (trigger) a workflow
- workflow.describe - Read a workflows contents
- workflow.validate - Validate a workflow's syntax and logic
- workflow.delete - Delete an existing workflow
- workflow.upload - Upload a new workflow to Kubiya
- integration.enable - Enable a new integration
- integration.disable - Disable an existing integration
- integration.list - List available integrations
- secret.list - List secrets stored in Kubiya
- secret.delete - Deleta a secret
- action-store.list - List action stores currently installed
- action-store.add - Add a new action store
- action-store.delete - Delete an installed action store
- action-store.describe - View the action contained in an action store
- event.list - List events
- event.get - Get a specific event
- trigger.create - Add a new trigger
- permissions.approve - Approve permissions


### Availalble Workflow IDs

All workflows that have been uploaded to Kubiya can be assigned to a user.

## Policy Examples

### Grant a user access to a specific workflow

To grant our user 'bob@jobswizzle.com' access to the 'hello_world' workflow we would issue the command:

```bash
kubiya policy create --policy-name bob-policy 
    --workflow-ids hello_world --allowed-entity bob@jobswizzle.com
```


