# Frontend generator from CUE schema

## Problem

The descriptive world of Kubernetes and other infrastructure-as-code tools is ruled by the written code and therefore often, the command line. There are many users, who prefer GUI for managing their stack. Building a GUI for the cloud-native tools is a tedious task. The team behind each of these tools puts a lot of effort into writing such a GUI and not many building blocks can be reused. However, the use-case is always the same - generate GUI that reflects the code configuration.

## Solution

This is a proposal to utilize the CUElang's native feature, schema validation as a starting point for GUI frontend generation. CUElang is getting popular in the Infrastructure-as-Code world. We are internally assessign it for input manifest data validation in the [Claudie](https://www.github.com/berops/claudie) project.

Having the schema which describes all the input fields, structures, data validation (e.g. min/max values, list of accepted values), one should have enough information to generate a GUI, that would allow to produce manifests, conforming to the schema. From there, it's a known task, to embed such a frontend into a larger GUI app, with specific design, authentication/authorization barrier, etc. As a result, the frontend generator can be embedded this way and offer a full GUI experience, which would dynamically reflect future schema evolution.
