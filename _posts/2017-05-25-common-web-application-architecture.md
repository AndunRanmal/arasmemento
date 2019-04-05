---
layout: post
title:  "Common Web Application Architecture"
author: andun
categories: [ Technology ]
tags: [web, architecture, ]
image: assets/images/webarchitecture.jpg
---


A web applications is an application that a user can accessed through a web browser.  The user creates HTTP request through the browser and request for resources to map for that url in web servers. Then the resource is rendered as an HTML page and give the response to the browser which the browser can displayed. The whole rendering/ process happens after getting a HTTP request processes in the server side of the web application. To explain this server side logic web application architectures are presented. These architectures consists of several number of layers.  Generally a common web application architecture consists with three layers as in the below diagram. Those layers named as presentation layer, business layer, and data layer. As it is three layers this web server architecture is named as three-tire architecture.

![walking]({{ site.baseurl }}/assets/images/webarchitecture1.png)

Presentation layer is the layer which interact with the user/browser and it contains with the functions which user interactions are managed. Generally presentation layer consists of UI and UI logical components to bridge with the business layer. Usually these components are in both client-side and the server-side

Business layer consists of the core functionality of the system. It encapsulated the business logic on the system. Having this layer allows to centralize the business core functionalities and reuse them in several location in different times. And also this make the system easy to maintain and do the functional testing as well. Contains different components as logics, workflows and entities.

Data layer provides the data hosted within the system boundaries. Having different layer for data makes the application more easy to maintain and configure.

Having a service layer is a common approach to use services to expose business functionalities of an application.

In the following sub topics we’ll be discussed about the subcomponents of common web application architecture and technologies, tools, frameworks, and libraries regarding those components.

Browser:

Web browser is a software application which use to receive, transfer and present informations in World Wide Web. These informations are found by the URL/URI. There are many types of browsers. Chrome, Firefox, Internet Explorer, Safari, Opera are the popular once. There are some advantages and disadvantages when using these browsers, like google chrome uses your RAM in a large amount but, it is one of the fastest web browser which supports almost all the hTML5 tags.

What actually browser does is, it renders the marked up content such as HTML and XML and formatting information such as css and xsl. A browser may wait until all the data get loaded to render or begin the rendering process before the all data get loaded.

Presentation layer:

Includes two components as UI components and UI process components. The UI components deal with the client side while UI process components deals with the server side. The advantage of having a separate presentation layer is able to change the appearance of the content without changing any business logic or data.

Frameworks: MVC, Ionic, REST, Apache Struts, Bootstrap, Apache Tiles

Libraries: Ajax, Jquery, JqueryUI, Backbone.js

Technologies: HTML5, CSS3, Javascript, EcmaScript, AngularJS, ReactJS, JSON

Business layer:

Include several components as application facade, business workflows, business entities, and business components. Application facade is the component that is responsible for calling the domains modal and get information to the presentation layer. Also it combines several business logics and provide an interface to connect those with the external user.

Business logic components defines retrieval, processing, transformation and management data, business policies, and rules and ensures data validity and consistency. For the easiness of the usage it is again divided into two components as business workflows and  business entity. Business workflow components contact with the business process components and perform operations with the use of business logics. While business entity components encapsulate the business logics a7nd functions to represent to the external parties.

Frameworks:  Meteor.JS, Express.JS, Codeigniter, Laravel, Spring MVC, Symfony, .NET, RubyOnRails, Django,

Libraries:  

Technologies: NodeJS, PHP, Java, C++, C#,  Python, Ruby

Data layer:

There are several components as data access components, data helpers/utilities and service agents. Data layer contains the necessary logics that wants to access the data. It design the entity objects that data object can be populate to transfer data between layers of the application architecture and to update data objects. Data access components in the data layer centralized the common data access functionality and easy to maintain the system and to configure.

Service agents implement data access components that isolate functionalities to call from the application. This may also  provide other services as caching, offline support.  

Frameworks:  ORM(Object Relation Mapping),   

Libraries:

Technologies:  

Cross cutting:

Many functionalities carried out by the application needs more than one layer. Crosscutting component implements specific kind of functionality to access those functionalities through one layer. Mainly there are three components as security, operational management, communication.

Security component performs the authentication, authorization and validation. While operational management include exceptional handling policies, logging, performance counters and configuration. Communication component include the components that communicated with other services and applications. Mainly this layer is to fulfill non-functional requirements.

Technologies: OAuth, OpenId, Grunt, Maven, LDAP

Data Sources:

Data sources is the database server, which provides database services like data manipulation to the web application.

Technologies: Mysql, MongoDB, SQLite, Oracle,   

Service Layer:

When providing application functionalities through a services it is important to have a separate layer for services. Usually there are two components include init. They are services interface and message types.This layer is connected to the web server externally. This layer increase the efficiency by maximizing the reusability and also by reducing the round trip time.