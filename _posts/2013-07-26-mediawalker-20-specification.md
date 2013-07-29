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

This document provides the specification of the API which can be used for developing devices, applications or services to interact with any social media service running on top of a MediaWalker engine 2.0 or above. The core are implemented as a set of RESTful API which you can be access anywhere from Internet via the http protocol, which can be called by almost any computer language, such as Jacascript, Java, php, C#, Ruby, Python, and so on.


### What is MediaWalker?

MediaWalker is a Platform as a Service (PaaS) for a peer-to-peer social media network. Not only provide a flexible and high-availability cloud service for media sharing, it also provides a non-blocking peer-to-peer message communication for operators to implement their business logic and connecting all the workflows together. Meanwhile, the respective API will be available for developers to implement applications or services on desktops, websites, mobile devices, or event sensors or any IoT, such as printers or any Arduino devices.

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

It runs on a large message queuing system in order not to blocking any API request.

### Specification

The following document describes 2.0 of the MediaWalker API.

Basically all API are defined under three categories, resource, data type, service and community category. Resource category includes printers, files, advertisement. Data type category are used to define some sharing data types, such as license, authentication, account, application and so on. Community category is designed for managing users accounts and provide a easy way to interact with popular social networks, like Facebook, Google+, and twitter accounts. These users account can be assigned treat as a content publisher, an application or service developer, or a regular user. The last category is a list of built-in services, such as global search, notification, chat rooms and application marketplace services.

## Resource Category

Where these resource information, permission or their current status can be access or interact through these API.

**Printer**

    printer
       /-status
        -info
        -location
        -owner
        -stream


**File**

    file
       /-license
        -owner
        -permission
        -downloads
        -likes
        -comments
        -cost


**Advertisement**

    advertisement 
       /-publish
        -subscribe
        -unsubscribe
        -stream


**Search**

    search
       /-filter



## Data type Category

Most of resource are related to each other with some formats for data types, there fore users retrieve these data types information through these API. 


**License**

    license
       /-name
        -reversion
        -type
        -notation


**Authentication**

    auth
       /-auth_key


**Account**

    account
       /-name
        -account
        -password


**Application**

    application
       /-category
        -owner
        -rated
        -updated
        -advertisement_list
        -redeems
        -search



## Community Category

**User**

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


**Publisher**

    publisher
       /-files
        -name
        -address
        -contact
        -bank_account


**Developer**

    developer
       /-applications
        -auth_keys


**Group**

    group
       /-chat
        -info
        -rss


**Search**

    search
       /-filter



## Service Category


**Global Search**

    global_search
       /-filter


**Notification**

    notification
       /-post
        -add_observe
        -remove_observe
        -time_stamp
        -stream


**Chat**

    chat
       /-room
        -join
        -rss


**Application Marketplace**

    marketplace
       /-category
       /-search
       /-promotion



### Summary

**CONFIDENTIAL: [TOP SECRET].**

  [john gruber]: http://daringfireball.net/
  [1]: http://daringfireball.net/projects/markdown/
  [source code]: http://www.attacklab.net/showdown-v0.9.zip
  [TOP SECRET]: ?blank=1 "Clear all text"
