+++
title = "Managing Resources with Tags"
date = 2021
weight = 1
chapter = false
+++

# Manage resources using Tags and Resource Groups

#### Overview

Tags are key and value pairs that act as metadata for organizing your AWS resources. With most AWS resources, you have the option of adding tags when you create the resource, whether it's an Amazon EC2 instance, an Amazon S3 bucket, or other resource. This lab will walkthrough assigning resource **tags** and using **Resource Groups**.

#### Tag
Tags are words or phrases that act as metadata that you can use to identify and organize your AWS resources. A resource can have up to 50 user-applied tags. It can also have read-only system tags. Each tag consists of a key and one optional value.

Tags allow categorizing AWS resources in a variety of ways - such as grouping them by purpose, owner, or environment. This becomes useful when there are multiple resources of the same type, and you want to identify a specific resource based on some properties that have been assigned to it. 

#### AWS Resource Groups
**AWS Resource Groups** is the service that lets you manage and automate tasks on large numbers of resources at one time. 
In AWS, a _resource_ is an entity that you can work with. Examples include an Amazon EC2 instance, an AWS CloudFormation stack, or an Amazon S3 bucket. If you work with multiple resources, you might find it useful to manage them as a group rather than move from one AWS service to another for each task. \
A _resource group_ is a collection of AWS resources that are all in the same AWS Region, and that match the criteria specified in the group's query. In Resource Groups, there are two types of queries you can use to build a group: **Tag-based** and **AWS CloudFormation stack-based**.

#### Content
1. [Using tags](1-using-tags)
2. [Creating a Resource Group](2-resource-group)
3. [Resource Cleanup](3-cleanup)
