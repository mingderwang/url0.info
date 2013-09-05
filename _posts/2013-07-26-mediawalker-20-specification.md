---
layout: post
title: "MediaWalker2 Specification"
description: ""
category : spec
tagline: "Supporting tagline"
tags: [katdc]
---
{% include JB/setup %}

## Overview

This document provides the specification of the APIs which can be used for developing devices, applications or services to interact with the social media network which runs on top of a MediaWalker2 engine or above. The core is implemented as a set of RESTful APIs which you can be access anywhere from Internet via the http protocol, which can be called by almost any computer language, such as Jacascript, Java, php, C#, Ruby, Python, and so on.


### What is MediaWalker2?

MediaWalker2 is a integration Platform as a Service (iPaaS) for quickly implementing a social media network marketplace. Not only provide a flexible and high-availability cloud service for media sharing or trading, it also provides a non-blocking peer-to-peer message communication for operators to implement their business logic and connecting all their business workflows together. Meanwhile, the respective APIs will be available for developers to implement applications or services on desktops, websites, mobile devices, or event sensors or any IoT (Internet of Things), such as mobilephones or any Arduino devices.

For implementing most of the social media service features, MediaWalker2 includes some must-have modules to provide the basic functions, such as user account management with web identity federation, media (file) storage, meta data searching, and sharing, notification and messaging queuing, and so on. Beside the built-in modules, MediaWalker engine also provides some interfaces to communicate with existing Internet blobstore services, such as Amazon S3, SNS, SQS, etc. For more details about available modules in MediaWalker2 will be listed in the specification section.  


### What does MediaWalker2 Do?

MediaWalker2 basically acts as a middleware of a media social network service. Therefore, not only it will provide a social network accounts management and also provide APIs for developers to write variety of applications on top of it or distribute or share license or license free contents throughout social network and/or e-commerce services. Therefore, it also provide an authentication method for both applications and licensed contents management.

MediaWalker2 is design to runs on a cloud service, based on a large message queuing system and multiple web servers in order not to block any API request and provide the best customer users experience. All web engines are spread across to a clustering OSGI containers with a distributed caching. Most of non-critical data are stored in a NoSQL non-blocking database with an automatic backup in order to provide a none-stop and high reliability services.

MediaWalker2 contains a set of default built-in services for operators to provide up-to-date social media network services, such as notifications, chat rooms, a global search engine, and a marketplace for applications or contents free download or purchasing. 


### Specification

The following document describes MediaWalker2 APIs.

Basically all APIs are defined under three categories, resource, data type, service and community category. Resource category includes devices, files, advertisement. Data type category are used to define some sharing data types, such as license, authentication, account, application and so on. Community category is designed for managing users accounts and provide a easy way to interact with popular social networks, like Facebook, Google+, Yahoo and/or twitter accounts. These users account can be assigned treat as a content publisher, an application or service developer, or a regular user. The last category is a list of built-in services, such as global search, notification, chat rooms and application marketplace services.

## Resource Category

Where these resource information, permission or their current status can be access or interact through these APIs.

**Device**

    device
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

Most of resource are related to each other with some formats for data types, there fore users retrieve these data types information through these APIs. 


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
       -devices
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

### Mardown Examples

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


**CONFIDENTIAL: [TOP SECRET].**

  [KatDC]: http://www.katdc.com/
  [1]: http://daringfireball.net/projects/markdown/
  [source code]: http://www.attacklab.net/showdown-v0.9.zip
  [TOP SECRET]: ?blank=1 "Clear all text"
