---
layout: default
title: Secrets Syntax
nav_order: 5
parent: Syntax Guide
---
# Secrets Syntax

## Create a Secret

To create a secret use the following command:

```bash
kubiya secret create --secret-name <secret name> --secret-value <secret value>
```
Alternate:
```bash
kubiya secret create -n <secret name> -v <secret value>
```

## List all Secrets

To list all known secrets use the following command:

```bash
kubiya secret list
```

## Delete a Secret

To delete a known secret use the following command:

```bash
kubiya secret delete -n <secret name>
```

