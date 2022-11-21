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

Kubiya supports a variety of Action identifiers.  For a full list, please refer to the [Policy Syntax Guide](../Syntax-Guide/Policies/sg_policies.md)

### Availalble Workflow IDs

All workflows that have been uploaded to Kubiya can be assigned to a user.

## Policy Examples

### Grant a user access to a specific workflow

To grant our user 'bob@jobswizzle.com' access to the 'hello_world' workflow we would issue the command:

```bash
kubiya policy create --policy-name bob-policy 
    --workflow-ids hello_world --allowed-entity bob@jobswizzle.com
```


