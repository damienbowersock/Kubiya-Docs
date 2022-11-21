---
layout: default
title: Knowledge Syntax
nav_order: 2
parent: Syntax Guide
---
# Knowledge Syntax

## Create a Knowledge Topic

```bash
kubiya knowledge create --topic-name '<topic-name>' 
  --examples '<comma separated list of example statements>' 
  --workflow <workflow to launch> 
  --answer '<natural language response to user>'
```

## Listing All Knowledge Topics

To see what Kubiya has learned from you issue the following Kubiya CLI command:

```bash
kubiya knowledge list
```

## Delete a Knowledge Topic

To delete a Knowledge Topic issue the following Kubiya CLI command:

```bash
kubiya knowledge delete --topic-name <topic to be deleted>
```
