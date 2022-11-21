---
layout: default
title: Secrets Syntax
nav_order: 4
parent: Syntax Guide
---
# Secrets Syntax

## Create a Secret

To create a secret use the following command:

```bash
kubiya secret create --secret-name <secret_name> --secret-value <secret_value>
```
Alternate:
```bash
kubiya secret create -n <secret_name> -v <secret_value>
```

## List all Secrets

To list all known secrets use the following command:

```bash
kubiya secret list
```

## Delete a Secret

To delete a known secret use the following command:

```bash
kubiya secret delete -n <secret_name>
```

