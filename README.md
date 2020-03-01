# Rainbow Contact Center FAQ

Updated: 13 Feb 2020

 I have consolidated questions from all groups into a FAQ here. This document will be updated as and when there are new content.

* [Requirements](#req)
* [How to sign up as Rainbow Developer](#signup)
* [When registrating a Rainbow developer account, what should we put for the company name?](#devcoy)
* [In general, what type of customers use the Rainbow platform?](#custtype)
* [How do you want the simulated webpage to look like? Is there any specific company that we should simulate?](#coytype)
* [What are the common questions asked by the customers of the contact centre agents? (This is to allow us to understand the type of skills required by the agents.)](#qns)
* [What are the types of support users can make? (i.e technical support/ customer service support)](#cat)
* [Is there a minimum requirement on the Web UI? (How it looks etc)](#ui)
* [What are some use cases that you want us to have?](#usecase)
* [Is there any existing routing engine used by Rainbow?](#engine)
* [Can we use other 3rd party APIs?](#3rdparty)
* [Who assign the skill tags to the agents? Are agents allowed to edit their own skill tags?](#tags)
* [Are we required to set up User-Authentication? If not, is there a specification on the type Database?](#auth)
* [Are there APIs for us to implement queues when a user makes a request but all agents are occupied?](#queue)
* [How much traffic should the system support?](#traffic)
* [Some general advice](#advice)

## <a id="req"></a> Requirements

### Description
[Rainbow](https://www.openrainbow.com/) is a cloud communication platform providing unified communication services such as chat, audio and video calls . Rainbow is frequently used by contact center agents to handle support requests from customers. Rainbow also provides SDK and API for developers to build custom UC applications.

Contact center agents need a routing engine to organise incoming chat requests and voice calls from customers into queues and route them to available agents based on agent availability, skills etc.

### Objective
* To develop a routing engine that routes incoming support requests (chat and audio calls) to the right agent based on agent availability, skills etc.

### Deliverables
* A web page simulating customer's website where their users can request for support via chat or audio call.
* A routing engine that routes incoming chat and audio call requests to the right agent based on agent availability, skills etc

### Tools Required
* [Rainbow SDK](https://hub.openrainbow.com/)
* Any web frontend framework (e.g. Angular, React, JQuery, Vue etc)
* Node.JS

## <a id="signup"></a> How to sign up as Rainbow Developer
Please see step-by-step instructions [here](dev-signup-instructions-global.pdf).

## <a id="devcoy"></a> When registrating a Rainbow developer account, what should we put for the company name?
If possible, please prefix your company name with "SUTD20-" e.g. "SUTD20-mycompany"

## <a id="custtype"></a> In general, what type of customers use the Rainbow platform?
Generally, Rainbow is used by both business users and customers. e.g. in a company for communication between co-workers, between a company and their customers etc

## <a id="coytype"></a> How do you want the simulated webpage to look like? Is there any specific company that we should simulate?
You are free to choose any company you want to simulate. e.g.
* a telco that sells mobile phones and broadband (android phone, ios phone, fiber broadband etc)
* a bank serving both retail customers and investors (e.g. depositor, investors etc)
* a travel agency providing different types of tour packages (e.g. adventure tour, free & easy tour, europe tour etc)

Whatever company you choose, please make sure there is enough options so that you can showcase your routing engine capabilities

Don't spend too much time on the design of the simulated company page, the important part is the portion where the customer interacts with the agents

## <a id="qns"></a> What are the common questions asked by the customers of the contact centre agents? (This is to allow us to understand the type of skills required by the agents.)
Possible questions that customers might ask the company are:
* my handphone/broadband is not working
* i have an issue with my bill
* what is the current saving interest rates
* can you tell me more about your europe tour packages
* i want to make an appointment
* etc

Example categories could be hardware support, billing support, general enquiries etc

Example agent skills could be android skill, ios skill, billing skill, europe tour skill, investment skills etc

## <a id="cat"></a> What are the types of support users can make?
See answer to this [question](#qns).

## <a id="ui"></a> Is there a minimum requirement on the Web UI? (How it looks etc)
No.

## <a id="usecase"></a> What are some use cases that you want us to have?
* **Queueing support requests** i.e. there are not enough active agents to handle pending customer requests, how do you handle that?
* **Agent availability status** i.e. agents need to go offline (e.g. lunch, restroom) so you cannot route customer requests to them
* **Agent skills** i.e. customer requests on specific skills should be routed to agents that are trained in that skill whenever possible

## <a id="engine"></a> Is there any existing routing engine used by Rainbow?
* There is no routing engine in Rainbow now.
* Rainbow currently allow one-to-one chat/audio calls and group chat/audio calls.
* In Rainbow, groups are called bubbles (please see Rainbow documentation)
* You can dynamically create bubbles and add particpants to the bubble via the API

## <a id="3rdparty"></a> Can we use other 3rd party APIs?
Please check with me first if you intend to use other 3rd party API.

## <a id="tags"></a> Who assign the skill tags to the agents? Are agents allowed to edit their own skill tags?
Normally, skill tags of each agent are set by the contact center manager/supervisor. It is good to have a simple admin panel to assign skill tags to agents, but this is not compulsory. You may hardcode the skill tags of the agents too.

## <a id="auth"></a> Are we required to set up User-Authentication? If not, is there a specification on the type Database?
For customers requesting support, you don’t need them to create an account or to login. You can make use of Rainbow’s [Guest account](https://hub.openrainbow.com/#/documentation/doc/hub/users-in-rainbow) feature.

For agents, they should be using Rainbow accounts and the standard [web.openrainbow.com](https://web.openrainbow.com) as the portal to interact with customers.

## <a id="queue"></a> Are there APIs for us to implement queues when a user makes a request but all agents are occupied?
No, Rainbow does not provide that. You have to build your own.

## <a id="traffic"></a> How much traffic should the system support?
For the purpose of this project, there is no capacity requirement but you should be able to demonstrate the use case where customer request is more than the number of active agents.

## <a id="advice"></a> Some general advice
* Start with chat support first. if you have remaining time, then move to audio calls.
* For agents, there's no need to design/build a seperate webpage for them. just use the standard [web.openrainbow.com](https://web.openrainbow.com) interface. if you have remaining time, then feel free to do what you want.
* Keep track of your remaining time, don't set a scope so big that you can't finish the project. identify what are critical features and what are good-to-have features (or rank them in terms of priority)
