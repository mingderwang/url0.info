---
layout: post
title: "MediaWalker 2.0 Specification"
description: ""
category : spec
tagline: "Supporting tagline"
tags: [katdc]
---
{% include JB/setup %}

## Overview

This document provides a specification of the API which can be used from devices, applications or services to interact with any social media service running on top of a MediaWalker engine 2.0 or above. The core are implemented as a web API which you can be access anywhere from Internet via http protocol, which can be called by almost any computer language, such as Jacascript, Java, php, C#, Ruby, Python, and so on.


### What is MediaWalker?

MediaWalker is a Platform as a Service (PaaS) for a peer-to-peer social media network. Not only provide a flexible and high-availability cloud service for media sharing, it also provides a non-blocking peer-to-peer message communication for operaters to implement their bussiness logic and connecting all the workflows together. Meanwhile, the respective API will be available for developers to implement applications or services on desktops, websites, mobile devices, or event sensers or any IoT, such as printers or any Arduino devices.

For implementing most of the social media service features, MediaWalker 2.0 includes some must-have modules to provide the basic functions, such as user account management with web identity federation, media (file) storage, meta data searching, and sharing, notification and messaging queuing, and so on. Beside the built-in modules, MediaWalker engine also provides some interfaces to communicate with existing Internet blobstore services, such as Amazon S3, SNS, SQS, etc. For more details about available modules in 2.0 will be listed in the specification section.  

### Examples

**Sub-Directories**
If pages are defined in sub-directories, the path to the page will be reflected in the url.
Example:

    .
    |-- people
        |-- bob
            |-- essay.html

This page will be available at `http://yourdomain.com/people/bob/essay.html`


**Recommended Pages**

- **index.html**
  You will always want to define the root index.html page as this will display on your root URL.
- **404.html**


1. **Jekyll collects data.**
  Jekyll scans the posts directory and collects all posts files as post objects. It then scans the layout assets and collects those and finally scans other directories in search of pages.

2. **Jekyll computes data.**

### What does MediaWalker Do?



### Specification

The following document describes 2.0 of the MediaWalker API.


printer
/-status
   -info
   -stream
   -location
   -owner

resource
/-printers
   -files
   -applications
   -services


file
/-license
   -owner
   -permission
   -downloads
   -likes
   -comments

license
/-name
   -reversion
   -type
   -notation
   
user
/-real_name
   -username
   -password
   -email
   -files
   -printers
   -bank_account
   -social_networks
   -groups

publisher
/-files
   -name
   -address
   -contact
   -bank_account

developer
/-applications
   -auth_keys

auth
/-auth_key

application

group
/-chat
   -info
   -rss


social_network
/-name
   -account
   -password

service

advertisement 
/-publish
   -subscribe
   -unsubscribe
   -stream

search


### Summary
