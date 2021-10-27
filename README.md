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

Testing vpc.json...


Infrastructure as code issues:
  ✗ Security Group allows open ingress [Medium Severity] [SNYK-CC-TF-1] in VPC
    introduced by Resources > ELBSecurityGroup > Properties > SecurityGroupIngress[0]


Organization:      ben.laplanche.test
Type:              CloudFormation
Target file:       /Users/benlaplanche/workspace/snyk-iac-cloudformation/vpc.json
Project name:      snyk-iac-cloudformation
Open source:       no
Project path:      .

Tested vpc.json for known issues, found 1 issues


Tested 11 projects, 9 contained issues.
```
