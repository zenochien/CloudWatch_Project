---
title : "Getting Started with CloudWatch agent and collectd"
date : "`r Sys.Date()`"
weight : 1
chapter : false
---

# Getting Started with CloudWatch agent and collectd

#### Overview

Observability helps you understand the health, usage, performance, and customer experience for your workloads. Observability can support many use cases, from detecting incidents and supporting incident resolution, to understanding the impact of new features on your users and workflow. Establishing the right solution depends on being able to gather the right data for your situation. In this post you will explore the use of collectd and the Amazon CloudWatch agent to add to the metrics that can be gathered from Linux instances.

You will walk through a basic setup of collectd and the CloudWatch agent on an Amazon Elastic Compute Cloud (Amazon EC2) Linux instance. The CloudWatch agent can collect system-level metrics and logs from your Amazon EC2 instances, and supports the collection of additional metrics from collectd. The data you collect can help you understand the performance and usage of your resources, and make data driven decisions to support your customers and workloads.

To help you get started, you will use a simple example of collecting data about open files, and see how to install and configure both collectd and the CloudWatch agent using AWS Systems Manager (SSM) to allow you to manage this process across multiple servers. You can then explore metrics of relevance to you and configure collectd accordingly.


#### Content

1. [Introduction](1-introduce/)
2. [Prerequiste](2-prerequiste/)
3. [Metrics](3-metrics)
4. [cleanup](4-cleanup)

