---
layout: post
title:  "Serverless Architecture: Learn it, Perfect it and Evolve with it"
author: andun
categories: [ Technology ]
featured: true
tags: [web, serverless, serverless architecture, AWS, FaaS, BaaS ]
image: assets/images/serverlessarchitecture.jpeg
---

#### The Road to Serverless
It would not be wrong if I tell you the next awakening step of cloud computing is serverless. The evolution to serverless architecture from physical servers has not been an easy journey. In early years software was installed in mainframe type server computers and used their own data stores. With the time these physical servers were replaced by the virtual machines where it became possible to make copies of an entire physical machine.

And the next big thing in this journey was containerization. With the uprise of containers developer needed not to worry about the operating system and environment. As a result, they could focus more on the software, application code and dependencies.

<h4>Serverless, The New Buzzword</h4>

With the new serverless architecture, you just need to focus on the applications’ business logic, and should not need to worry about any infrastructure needs. And this leads to many more advantages which we will discuss later in this article.
Serverless architecture, the new buzzword has been around for the past few years and now it has been a reality. The adaptation rate for this tech is slower than any other new technologies. But with the time number has been increased with the awareness of the benefits of serverless architecture.

The term, Serverless Architecture may be confusing. Someone may think we are building an application which runs completely on the client side or probably distributed within different clients, without any serverside operation.

But is that a reasonable definition for an application builds on serverless architecture. No… Cloud Architecture specialists define this in [another way](https://martinfowler.com/articles/serverless.html).

>Serverless architectures are application designs that incorporate third-party “Backend as a Service” (BaaS) services, and/or that include custom code run in managed, ephemeral containers on a “Functions as a Service” (FaaS) platform.

As he explains more on serverless architecture, it denies the need of an always-on, pre-purchased compute capacity behind the application, unlike the traditional architecture. The containers which server-side logic has been written are stateless, and they are event triggered. With these facts its clear to us there is a server component in somewhere connected to these serverless applications.

There are many cloud vendors who provide these hosted services. And these companies have hugely invested in serverless. Amazon Web Services(AWS), Google Cloud Platform(GCP), Microsoft Azure, IBM OpenWhisk, Auth0 Webtask, Oracle Fn Project could be named as the giants in the serverless industry.

#### FaaS & BaaS

Two main components of the serverless architecture are FaaS and BaaS. As in the definition of serverless architecture describes the part of applications that are fully or significantly incorporated third-party, cloud-hosted services that are capable of managing server-side logic and state is known as BaaS. For an example, the developer gets unified lean access to services like database services like firebase, authentication services like Auth0, AWS Cognito. As a benefit with these services, developers can bring [rich client](https://www.techopedia.com/definition/16012/rich-client), fully functional application to the market in a very short period of time.

For some scenarios in application development, the developer needs to declare logics that needs much more computational power, unlike authentication or data querying. And also if these logics are more complex and time-consuming, it will not fit in the client side as well. To fulfill this kind of requirement serverless has introduced FaaS. So the developer could write and upload the backend logic and well-defined interface to invoke the backend logic with certain inputs. These functions run in stateless compute containers which are event triggered. Once these functions are implemented and deployed, cloud providers take care of the rest, which is where to run it and scale it up necessarily.

One of the most popular FaaS in the present serverless universe is AWS Lambda. And there are many more. As serverless become more and more popular cloud providers have given the capability to write these functions in several languages like Node js, Python, Java, and .NET.

Some could think that FaaS is the same as Platform as a Service(PaaS). Well, although there are some similarities between these two, there is a huge concept difference. FaaS takes PaaS concept into a next level. One of the main difference between FaaS and PaaS is when an application deployed as PaaS, it typically runs on the server all the time, but in FaaS it provides the capability to deploy single function or a part of an application. And it won’t be running at all until the function needs to be executed.

#### Pros & Cons

Serverless is not scary. There are many benefits when programmers develop with serverless architecture. As there is nothing perfect in this world, serverless is also has its own dark side. Although serverless has many pros than cons when getting into consideration.

##### Pros of serverless

* Scalable services — It is the ideal designing architecture for a scalable application. It automatically scales endlessly as it takes separate functions on your FaaS and runs them in separate containers

* Billing per invocations — Not like in traditional architecture models you ain’t paying for constant server availability. You just pay for the number of invocation made to your lambda. Thus your cost depends on the traffic on your serverless application

* Lower cost on human resource and hardware resource — As there is no much expensive hardware, no need of a human taskforce to maintain this hardware

* Focus much more on user experience — As there are lots of serverside services are provided with serverless computing, hence the engineering team could more focus on user experience features

* Fast delivery to market — Achieved by deploying smaller units of functions as features to end user

##### Cons of serverless

* Vendor lock-in — It’s not easy to migrate from one vendor to another, or you aren’t independent in choosing the coding language.

* Architectural complexity — Developer need to go through a learning curve and follow best practices to understand and develop flawless applications

* Lack of operation tools — Developer depends on different third-party vendors for monitoring and debugging, and still difficult in debugging distributed system and requires a significant amount of relevant metrics to identify the root cause

---

Originally published at slappforge.com on November 1, 2018.