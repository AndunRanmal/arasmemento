---
layout: post
title:  "Getting Started with React Native and AWS"
author: andun
categories: [ Technology ]
image: assets/images/first_step.jpg
---
##### Why React Native?
React native has become the future of mobile development and one of the trending framework for Android and ios app development. It is based on React, Facebooks' javascript library for building user interfaces targetting mobile platforms. And most of these user interfaces components could be shared among both ios and android. As with the asynchronous javascript interactions with the native environment inside this lovely framework, the outcome will be highly responsive smooth app with quicker load time than a typical hybrid app

##### Why AWS?
AWS is another trending topic/technology in the past couple of years as well as upcoming years with the new buzz word serverless. It provides you with multiple backend services such as authentication services, database services, so the developer could solely focus on business logic and user interfaces of the application and deliver a rich client, fully functional application to the market in a short period of time. 

As for my project, I intend to implement a serverless backend end with AWS resources. And I am going to explain step by step to develop a simple project with authentications. AWS has introduced AWS Amplify a declarative JavaScript library for cloud development with mobile or web applications to easily implement AWS features to your mobile app or web app. As Amplify library has divided into modules such as Auth. Storage, APIs, the developer can easily and quickly add features like Signup, MFA, Content management, serverless API integrations. So let's get started.

##### Getting Started…

###### Create react native project

If you refer react native docs you could see there are 2 methods to create your react native project. 
Using expo CLI quickstart
Using react native CLI quickstart
I’m going to use the 1st method using expo, as with expo tools, services and react native you can build, deploy, and quickly iterate on native iOS and Android apps from the same JavaScript codebase.
The first step is to install expo-cli globally

    npm install -g expo-cli 

Then run the following commands where you want to create your project `simple_auth_project`

	expo init simple_auth_project

CLI will provide you with two options to select a template. You can go with either of these. I am going with the first option as I intend to implement the only authentication with this article

	expo start
	
`a` to start your project with android device or `i` to start the project in ios

###### Adding Amplify 

There are 2 ways of using AWS Amplify. You can initialize your current project as an AWS amplify project and build your project and resources from scratch or either just use aws-amplify library and resources that already exist. On this article, I will be describing on building your project from scratch initializing the project as amplify project. 
Go to project 
    
    amplify init
