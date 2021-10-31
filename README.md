# Snyk Infrastructure as Code - Azure Resource Manager (ARM)

The Snyk Infrastructure as Code product can scan ARM templates for configuration issues.

[ARM](https://docs.microsoft.com/en-us/azure/azure-resource-manager) files can be a mix of JSON or Bicep formats.

## Demo

This repository contains a mix of valid configuration files, which contain a range of configuration issues.

You can see the results by running
`snyk iac test .`

A snippet of the output looks as follows

```bash
-------------------------------------------------------

Testing wordpress.json...


Infrastructure as code issues:
  ✗ SAS token can be used over insecure HTTP [Medium Severity] [SNYK-CC-TF-244] in Storage
    introduced by resources[2] > properties > supportsHttpsTrafficOnly


Organization:      yair.zohar
Type:              ARM
Target file:       wordpress.json
Project name:      snyk-iac-arm
Open source:       no
Project path:      snyk/snyk-iac-arm

Tested wordpress.json for known issues, found 1 issues


Tested 7 projects, 5 contained issues.
```
