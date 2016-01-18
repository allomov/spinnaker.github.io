---
layout: toc-page
title: User's Guide
id: user_guide
lang: en
---

* Table of contents. This line is required to start the list.
{:toc}

#Spinnaker User Guide

## Spinnaker Concepts ##

The following section introduces the terms used within Spinnaker. 

### Application-Centric Cloud Model ###

Spinnaker helps simplify cloud deployment by associating cloud objects with applications and projects.  

An **application** is the most atomic unit of deployment in Spinnaker. It represents a deployable that you would normally organize into a cloud image, container or similar mechanism. 

Cloud objects such as load balancers, security groups and autoscaling server groups are all organized under an individual application. Spinnaker enforces the naming conventions from Frigga, which help easily associate a cloud object with it's corresponding application.  

Spinnaker lets you group several applications into **projects**. One application can be tracked by several projects.  The project dashboard in Spinnaker provides a bird's-eye view that helps you distill interesting information across different applications in one place.

If configured properly, Spinnaker is able to manage resources in multiple **accounts** across multiple **cloud providers**. For example, you might want to create an account for sensitive billing information and one for general use. 

Additionally, you can group different clusters within your application across a **stack**. For a given application or set of applications, you might want to have a development, staging and production stack. 

### Execution Model ###

Spinnaker provides two distinct mechanisms to orchestrate your cloud deployments. 

A **task** is what happens when you make a change directly via the Spinnaker UI or by calling the API. For example, when you create a new application in the infrastructure screen or resize a server group in the clusters screen, a new task is created and tracked. 

A **pipeline** allows you to organize more complex cloud deployment instructions in a set of repeatable, automated **stages**.  Pipelines can be kicked off by hand, or listen to events from external sources like Jenkins via automated **triggers**. Spinnaker keeps track of pipeline **executions**, which are records of what happens each time a pipeline runs. 

## Managing Applications ##

This section describes how to manage and configure applications in Spinnaker.

## Project Dashboards ##

This section describes how you can make use of the project dashboards in Spinnaker to look at information across applications.

## Working with Cloud Objects ##

This section describes how you can use Spinnaker to navigate your resources on the cloud.

## Pipelines ##

This section shows you how to use deployment pipelines in Spinnaker.

## Using The Spinnaker API ##

This section describes how to access and interact with the Spinnaker API. 