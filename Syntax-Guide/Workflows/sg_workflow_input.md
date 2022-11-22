---
layout: default
title: Input
parent: Workflow Syntax
grand_parent: Syntax Guide
nav_order: 2
---
# Workflow Input Syntax Guide

### Input

#### Input Value Types (Required)

Input Types define the expected data type to be provided by the user, much like a data type when defining a variable in most programming languages.

The following input types are supported:

* `text`: A text input. This is the most common input type - it is used to capture a single text input from the user.
* `numeric`: A numeric input. This input type is used to capture a single numeric input from the user.
* `boolean`: A boolean input. This input type is used to capture a single boolean input from the user.
* `enum`: An enum input. This input type is used to capture a single enum input from the user.
* `date`: A date input. This input type is used to capture a single date input from the user.
* `time`: A time input. This input type is used to capture a single time input from the user.
* `datetime`: A datetime input. This input type is used to capture a single datetime input from the user.

#### Input Prompt (Required)

A Prompt allows Kubiya to provide text output to the user.  This may be asking a question, providing a response etc.  Prompts are defined simply as:

```yaml
prompt: you prompt here
```

Prompts may include variables that are referenced by the 'id' of the step that they are created in.  

```yaml
prompt: The users name is ${step id here}
```

#### Input Validators

Input validators confirm that the data provided by the user conforms to the standard expected in the workflow.

The following input validators are supported:

* `text_longer_than`: Validates that the input is longer than the specified length.
* `text_shorter_than`: Validates that the input is shorter than the specified length.
* `min`: Validates that the input is greater than or equal to the specified value.
* `max`: Validates that the input is less than or equal to the specified value.
* `is_integer`: Validates that the input is an integer.
* `is_float`: Validates that the input is a float.
* `is_date`: Validates that the input is a date.
* `is_time`: Validates that the input is a time.
* `is_datetime`: Validates that the input is a datetime.
* `is_enum`: Validates that the input is an enum.
* `is_boolean`: Validates that the input is a boolean.
* `is_email`: Validates that the input is an email.
* `is_url`: Validates that the input is a URL.
* `is_phone_number`: Validates that the input is a phone number.
* `is_ip_address`: Validates that the input is an IP address.
* `is_ipv4_address`: Validates that the input is an IPv4 address.

#### Input Additional Properties

The following additional input properties are supported:

* `possible_values`: A list of possible values for the input. This property is required for `enum` input types.
* `default_value`: The default value of the input. This property is optional.
* `required`: Whether the input is required. This property is optional. Default value is `true`.

### Input Examples

#### Single Input

```yaml
id: name
    prompt: Please enter your name.
    type: input
    value_type: text
```

#### Single Input with Validator

```yaml
id: name
    prompt: Please enter your name.
    type: input
    value_type: text
    validators:
      - text_longer_than: 4
```

#### Required Single Input with Validator

```yaml
id: name
    prompt: Please enter your name.
    type: input
    value_type: text
    validators:
      - text_longer_than: 4
    required: true
```