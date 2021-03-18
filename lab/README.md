In order to get you familiar with this starter kit and creating services on IBM Cloud, this lab will walk you through the steps of setting up a sample application.

In addition to this README, the starter kit includes [a lab to get started with your own Node-RED instance](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/tree/master/lab) and a [JSON file of example integrations](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/zero-hunger-node-red-flows.json).

## Table of Contents
* [Create your IBM Cloud Account](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/README.md#create-your-ibm-cloud-account)
* [Create a Node Red Instance](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/README.md#create-a-node-red-instance)
* [Integreate a Cloudant Database](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/README.md#integrate-a-cloudant-database)
* [Creating your Twilio SMS integration](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/README.md#creating-your-twilio-sms-integration)
* [Creating a Telstra SMS integration](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/README.md#creating-a-telstra-sms-integration)
* [Integrating with Open Weather Map](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/README.md#integrating-with-open-weather-map)
* [Creating a Dashboard Visualization](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/README.md#creating-a-dashboard-visualization)
* [Additional Resources](#creating-a-dashboard-visualization)

## Creating your IBM Cloud Account
1. Visit the [IBM Cloud Registration page](https://cloud.ibm.com/registration) and fill out your email and password
2. Check your email for a verification email and click the confirmation link
3. Once your account has been activated, visit your [IBM Cloud Dashboard](https://cloud.ibm.com/). You can always get back to this location by clicking "IBM Cloud" in the upper left of any page.
4. To add a service, click the blue "Create" in the upper left corner of the dashboard.

## Creating a Node Red Instance
1. Visit your [IBM Cloud Dashboard](https://cloud.ibm.com/).
2. In the upper right corner click **Create Resource**.
![Create Resource button](images/nr-1.png)
3. You're now looking at the IBM Cloud Catalog, a list of software and services that you can automatically deploy on the cloud. Find the **Search** box and type `node` to filter down the services. Select **Node-RED App**.
![Search box](images/nr-2.png)
4. For our Node-RED isntance, we will use the Cloudant database. Cloudant is a scalable, distributed cloud database based on Apache CouchDB. This page includes links to the [Cloudant Docs](https://cloud.ibm.com/docs/Cloudant) and [Cloudant API reference](https://cloud.ibm.com/apidocs/cloudant). Click **Get Started** to continue.
![Get started](images/nr-3.png)
5. You're now on the **Create** tab. You'll notice that an application name has been chosen for you, but you can feel free to change it. At the bottom of the page, make sure **Pricing plan** is set to **Lite**. This ensures you will not be charged for the application. Click **Create**.
![Application settings](images/nr-4.png)
*Note: You can only have one Cloudant instance using the Lite plan. If you have already got an instance, you will be able to select it from the Pricing plan select box. You can have more than one Node-RED Starter application using the same Cloudant service instance.*
6. After a few moments, your Cloudant database will finish provisioning and will be available for use. At this point, we will be able to create our Node-RED app and store it in the Cloudant database. Click **Deploy your app** to continue.
![Application settings](images/nr-4.png)

*TBD: CICD Pipeline*

10. Next, we'll load our example code into the Node-RED environment. Since Node-RED stores its configuration as JSON, we can do that by copying and pasting a JSON file. In the top right of your Node-RED environment, click the **triple-line menu** and select **Import**. 
![Settings Menu](images/nr-10.png)
11. Now, we'll copy the JSON from this starter kit. This JSON is stored in `zero-hunger-node-red-flows.json`. You can access that file [here](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/lab/zero-hunger-node-red-flows.json). **Copy** this json to your computer clipboard, and **Paste** it into the Node-RED import window. Then click **Import**.
![Import Dialog](images/nr-11.png)
12. Congratulations! Your Node-RED environment is now populated with a number of flows that will help you create your Call for Code application. In the remainder of this lab, we'll cover flows that we have just imported and explain how they can be used together to create more complex applications.

Further reading:
* [How to Create a Node-RED Starter Application on IBM Cloud](https://developer.ibm.com/components/node-red/tutorials/how-to-create-a-node-red-starter-application/)

## Integrate a Cloudant Database

In the last step, we created a Cloudant databae in order to store our Node-RED application. While we are only able to create one Cloudant database on our IBM Cloud Lite tier, we can store information other than our Node-RED application in the same database.

![Cloudant Database Flow](images/cloudant-1.png)

*TBD: Database flow walkthrough*

Further reading:
* [Connecting to IBM Cloud services from Node-RED](https://knolleary.net/2018/06/05/connecting-to-ibm-cloud-services-from-node-red/)
* [Connecting to a Cloudant Database in Node-RED](https://medium.com/@ml4den/connecting-to-a-cloudant-database-in-node-red-37239bfc9ede)

## Creating your Twilio SMS integration

![Twilio Flow](images/twilio-1.png)

Since local farmers often do not possess smartphones, we anticipate that SMS will become a critical component of communications in many Call for Code solutions. To facilitate this, we've created a sample Twilio SMS flow, along with additional resources below.

1. In order to get started, you'll need a Twilio account. [Sign up for Twilio here](www.twilio.com/referral/lup4VV).

*TBD: Twilio flow walkthrough*

## Creating a Telstra SMS integration

When addressing the Australian market, an integration with Telstra can facilitate communication with local stakeholders. This section will cover our example Telstra Node-RED flow.

1. [Register for your TelstraDev account here](https://dev.telstra.com/tdev/user/register). This will require you to create a Telstra ID, if you don't already have one.
Your account automatically gives you access to the Free Trial, which provides an Australian Virtual Mobile Number to send your first 100 messages to up to 5 recipients. If you would like the paid account with full features, please proceed to ['Create a Company'](https://dev.telstra.com/company-add) (For Australian ABN holders only).
2. Once you have verified your account, you will be able to access your apps & keys under Develop-> [My Apps & Keys](https://dev.telstra.com/user/me/apps)
3. You may leverage the [Messaging API SDKs in GitHub](https://github.com/telstra) for multiple programming languages, or download our [Postman Collection](https://dev.telstra.com/content/messaging-api#section/Getting-Started/Run-in-Postman)
4. Get an OAuth2 token with the API keys. Each set of API keys will provide you a Virtual Mobile Number to send and receive messages with the API.
5. Use GET/Subscription to provision an Australian virtual mobile number. You will need one of these to send or receive messages via SMS or MMS. [Check the TelstraDev docs for details](https://dev.telstra.com/content/messaging-api#operation/createSubscription)
6. If you are using the Free Trial, you will need to register the 5 destination mobile numbers (known as `bnum`'s) that you will be able to send test messages to. [Check the TelstraDev docs for details](https://dev.telstra.com/content/messaging-api#operation/freeTrialBnumRegister)
7. In a seperate flow, put together the desired message payload. e.g images, iot triggers, text responses.
8. To send an SMS, make a POST call to the `https://tapi.telstra.com/v2/messages/sms` endpoint with the destination number as `to` and message payload in step 7 as `body`.

Here is an example node-red flow that allows you to get an OAuth token, provision your mobile number, and add in the destination numbers you wish to send to (aka B-Nums).

![Telstra Flow](images/NodeRed-Flow-1-Prov-&-B-Num.png)

This node-red flow sends a message from the number provisioned above that uses a message body created in another part of your node red flow.

![Telstra Flow](images/NodeRed-Flow-4-Send-SMS.png)

### Further reading:
* [Telstra Messaging API documentation](https://dev.telstra.com/content/messaging-api)
To see this in action with previous Node-Red and IoT integrations, check out these repos: 
* [Control your IoT device remotely via SMS](https://github.com/MichelleHowie/TelstraDevArduinoNodeRedBlink) 
* [Ask for IoT environmental sensor info via SMS](https://github.com/MichelleHowie/IoTSensorData_OnDemand)
* [Send automatic SMS alert when your IoT device is dropped](https://github.com/MichelleHowie/Arduino-MKR-IMU-Fall-Detect)
* [Example Flow: A Node-RED flow to send SMS messages via the Telstra Messaging API](https://github.com/brendan-myers/node-red-contrib-telstra-messaging)

## Integrating with Open Weather Map

![Open Weather Map Flow](images/owm-1.png)

*TBD: Waiting on keys*

The Weather Company is an IBM business that provides a number o 

## Creating a Dashboard Visualization

![Dashboard Flow](images/dashboard-1.png)

*TBD: Dashboard explanation*

## Additional Resources
* [API Documentation Links](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/README.md#api-integration-documentation)
