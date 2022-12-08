---
layout: default
title: Policy Syntax
nav_order: 4
parent: Syntax Guide
---
# Policy Syntax


## Create a Policy

To create a policy, we must associate a set of allowable actions with a user's login email.  This can be done at the Kubiya CLI using:

```bash
kubiya policy create --policy-name <policy name> 
    --action-ids <comma-seperated list of allowed actions>
    --workflow-ids <comma-serperated list of allowed workflows>
    --allowed-entity <user login email>
```

### --action-ids Flag

Action IDs supported for the '--action-ids' flag are as follows:

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


### --workflow-ids Flag

Any available workflow may be used with the '--workflow-ids' flag.  Please see the [Workflow Syntax](../Workflows/sg_workflows.md) for the command to list workflows.

### --allowed-entity Flag

The 'allowed-entity' flag is used to identify what user or group of users the policy applies to.  A valid user's login email address is used to identify a single user that the policy is assigned to.  If an identity provider is configured to authenticate to Kubiya, a role may be used to grant access to multiple users that possess that role.

## List all Policies

To view a list of all policies, use the following command:

```bash
kubiya policy list
```

## Describe a Policy

Describing a policy allows the operator to inspect a currently defined policy.

```bash
kubiya policy describe -p <policy name>
```

## Delete a Policy

```bash
kubiya policy delete -p <policy name>
```

