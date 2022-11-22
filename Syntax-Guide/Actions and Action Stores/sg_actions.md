---
layout: default
title: Action Syntax
nav_order: 2
parent: Syntax Guide
---
# Action Store Syntax Guide

## Import an Action Store

```bash
kubiya action-store add --image-url <your image url> --name <action store name>
```

## List all Action Stores

```bash
kubiya action-store list
```

## Describe an Action Store

Describing an Action Store will all Actions that can be called from that store.

```bash
kubiya action-store describe <action store name>
```

Note: Many Action Stores contain hundreds of actions.  Therefore it may be beneficial to pipe the 'describe' function through 'more' to paginate the output as follows:

```bash
kubiya action-store describe <action store name> | more
```

## Bundle an Action Store


## Delete an Action Store

To delete a given Action Store, simply issue:

```bash
kubiya action-store delete <action store name>
```
