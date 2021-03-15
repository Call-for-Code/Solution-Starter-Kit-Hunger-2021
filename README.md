# Call for Code solution starter kit: Zero hunger

[![License](https://img.shields.io/badge/License-Apache2-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![Slack](https://img.shields.io/badge/Join-Slack-blue)](https://callforcode.org/slack)

The Zero Hunger Call for Code starter kit helps developers build applications to addresss the real-world challenge of global hunger under the Climate Change theme in 2021. This starter kit will give you the tools to connect farmers, cooperatives and consumers through a potential technology solution for the problem of global hunger.

## Contents

1. [Background](#background)
1. [Demo video - TBD](#demo-video)
1. [The architecture - TBD](#the-architecture)
1. [Getting started - TBD](#getting-started)
1. [Contributing - TBD](#contributing)
1. [Versioning](#versioning)
1. [Authors](#authors)
1. [License](#license)
1. [Acknowledgments](#acknowledgments)

## Short description

### What's the problem?

8.9% of the global population is suffering from hunger. The UN Sustainable Development Goal #2 of Zero Hunger sets ambitious targets to profoundly change the global food and agriculture system and give more people a regular access to safe, nutritious, and sufficient food to reach zero hunger by 2030. 

Much of the world’s food is grown by small scale independent farms and distributed through local community co-operatives who sell the surplus produce. The co-ops are a central point for quality control, deliveries and enabling food commodity markets. These co-ops face a myriad of logistical challenges to get the right food, to the right places, with minimal time and cost. 

### How can technology help?

By bringing the paper ledgers of food co-ops online, the communities can harness data insights from their environment for better crop resilience and overall yield for sustainable food production systems at the grassroots. More crops mean better access to food for the community.
Rural farmers may not have the access to network connectivity, digital literacy, language or appetite for risk to adopt tech solutions directly, so the co-ops become the pivotal point of innovation. 

### The idea

Co-operative systems can be digitised and enhanced to improve access to nutritious food in local communities (especially those suffering from acute hunger). By aggregating and analysing market, transport, demand, horticultural and environmental data they can optimise productivity, reduce overheads and decrease volatility in the supply chain of these farming communities that can address the global hunger crisis. 

## Demo video - TBD

[![Watch the video](https://github.com/Call-for-Code/Liquid-Prep/blob/master/images/readme/IBM-interview-video-image.png)](https://youtu.be/vOgCOoy_Bx0)

## The architecture

![Co-operative Control Center](https://github.com/Call-for-Code/Solution-Starter-Kit-Hunger-2021/blob/master/architecture_diagram.png)

1. User uses their non-smart phone camera to capture a photo of their product yield to send for quality testing and analysis.
2. User sends a camera image and/or a text message through their non-smart phone messenger.
3. The image and/or message is redirected to the Twilio Programmable Messaging service or to the Telstra Messaging service for users located in Australia.
4. Twilio Programmable Messaging or Telstra Messaging will forward the message to the Node-RED app hosted on IBM Cloud.
5. The Node-RED app interacts with Watson Machine Learning to get the response.
6. Cloud Object Storage is provisioned to receive the images and/or message data.
7. The image and/or message data is added to the available Cloud Object Storage.
8. Watson Machine Learning does the necessary computations and returns a response.
9. The Node-RED app processes the response and converts it to user-readable format and forwards to the Co-operative control center dashboard. (Optional: to Twilio)
10. The response is then sent to the control center dashboard UI.
11. The Co-operative admin is able to view the response, assess the quality of the product yield, accept & manage purchase orders, and manage client credits for payment via the control center dashboard.
12. (Optional: Twilio forwards this message as a reply through their messenger)
13. (Optional: The user will receive this as a response from Watson Machine Learning service on their phone's messenger)

## Getting started

You can create a solution based on the proposed solution architecture above by exploring the following resources on the [IBM Developer](https://developer.ibm.com/) site. I'm 

### Example Solutions

Here are some ideas for solutions that this starter kit can help you build:

#### A cooperative can aggregate data from farmers via phone cameras and sms to analyze the data in order to optimize productivity by 30% through knowledge sharing.

#### A cooperative can manage farmers’ accounts, including credits, to facilitate trade and distribution of funds in order to create transparency among transactions and reducing overhead and labor by ~40%.

#### A cooperative leader can find nearby markets to sell their products for the optimal price to maximize profit by ~20–40%.

#### A cooperative can connect with other cooperatives to optimize refueling routes and trips to lower transport costs by ~50%.

#### A cooperative can use weather and trend data to provide farmers with personalized plans regarding when to plant, fertilize, and irrigate to increase the farmer’s yield by ~25%.

#### A cooperative can provide recommendations on the best crops to grow based on their market, geographic, and environmental patterns to decrease exposure to income loss and volatility by ~30%.

### Tutorial - TBD

### Resources

#### Artificial intelligence

Use AI to create apps that accelerate, enhance, and scale the human experience.

* [Link 1](https://developer.ibm.com/callforcode/technical-library/)
* [Link 2](https://developer.ibm.com/callforcode/technical-library/)
* [Link 3](https://developer.ibm.com/callforcode/technical-library/)

#### Data science

Analyze structured and unstructured data to extract knowledge and insights related to urgent issues.

* [Link 1](https://developer.ibm.com/callforcode/technical-library/)
* [Link 2](https://developer.ibm.com/callforcode/technical-library/)
* [Link 3](https://developer.ibm.com/callforcode/technical-library/)

#### Internet of Things

Collect and analyze device sensor data to take corrective or preventative action automatically.

* [Link 1](https://developer.ibm.com/callforcode/technical-library/)
* [Link 2](https://developer.ibm.com/callforcode/technical-library/)
* [Link 3](https://developer.ibm.com/callforcode/technical-library/)

#### Platform development

Identify the right environment, software, and runtime to power and scale your solution.

* [Link 1](https://developer.ibm.com/callforcode/technical-library/)
* [Link 2](https://developer.ibm.com/callforcode/technical-library/)
* [Link 3](https://developer.ibm.com/callforcode/technical-library/)

#### Data sets

These public data sets provide information on the problem.

* [Link 1](https://developer.ibm.com/callforcode/technical-library/)
* [Link 2](https://developer.ibm.com/callforcode/technical-library/)
* [Link 3](https://developer.ibm.com/callforcode/technical-library/)

#### NGO documents

These are the go-to documents for measuring impact and progress against the key issue.

* [Link 1](https://developer.ibm.com/callforcode/technical-library/)
* [Link 2](https://developer.ibm.com/callforcode/technical-library/)
* [Link 3](https://developer.ibm.com/callforcode/technical-library/)

## Contributing - TBD

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests.

## Authors

* **Michelle Howie** - *Problem Statement & Description* - [Twitter](https://twitter.com/michelle2minhye)
* **Jenna Ritten** - *Architectural Diagram, Flow & Resources* - [Twitter](https://twitter.com/jritten)
* **David Nugent** - *Outline & Resources* - [Twitter](https://twitter.com/drnugent)

See also the list of [contributors](https://github.com/Call-for-Code/Starter-Kit-Template-2021/graphs/contributors) who participated in the creation of this starter kit.

## License

This starter kit is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Based on [Billie Thompson's README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2). Thank you Billie!
