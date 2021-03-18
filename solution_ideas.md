# Solution ideas

This is a list of potential solutions that teams can use the Zero Hunger starter kit to implement. Please feel free to use these ideas, or develop an idea of your own.

We encourage you to choose clear, measurable outcomes, even if you are not able to prove they can be achieved at the outset. Additionally, think about how you can utilize the integrations provided by our starter kit, and which additional integreations you'll need to create on your own.

Each of our solution ideas is presented in the following format:

```diff
! Who?
+ What will they do?
- To achieve this measurable outcome (wow!)
```

## Solution idea: Image sharing

Farmers use non-smartphone devices to communicate in order for co-operatives to create a database of information that can be used to analyze trends.

```diff
! A co-operative
+ can aggregate data from farmers via phone cameras and sms to analyze the data 
- in order to optimize productivity by 30% through knowledge sharing.
```

To implement this solution, you can use the SMS gateway integration provided by the starter kit to allow farmers to send messages and images to a central database, for example, Cloudant and IBM Cloud Object Storage. You could further analyze the information using IBM Cloud Pak for Data Watson AI/ML offerings.

## Solution idea: Accounting and credits

Farmers work with co-operatives to buy and sell goods using credits and don't have a effective way of accepting or processing payments.

```diff
! A co-operative
+ can manage farmers’ accounts, including credits, to facilitate trade and distribution of funds in order 
- to create transparency among transactions and reducing overhead and labor
```

To implement this solution, you can use the SMS gateway integration provided by the starter kit to provide real-time messaging between farmers and cooperatives. As a stretch goal, you might find and aggregate real-time price and market data, and optionally, integrate a distributed ledger, such as blockchain, to track transactions.

## Solution idea: Weather data

Co-operatives can aggregate and distribute data to their farmers in order to improve yields.

```diff
! A co-operative
+ can use weather and trend data to provide farmers with personalized plans regarding when to plant, fertilize, and irrigate
- to increase the farmer’s yield by ~25%.
```

To implement this solution, you can use the starter kit to integrate with The Weather Company's data to track weather patterns and use the SMS gateway to communicate to farmers when to plant. There is a Weather Channel Notification API that can be used to notify farmers of adverse conditions. If needed, your app can use a Cloudant database to store data. You can use machine learning to analyze trends from weather data specific to your area.

## Solution idea: Optimize trips

Co-operatives can help farmers decrease their fuel costs, which can decrease maintenance and increase profits.

```diff
! A co-operative
+ can connect with other cooperatives to optimize refueling routes and trips 
- to lower transport costs by ~50%.
```

Implementing this application using our starter kit, you can begin with an SMS gateway communication with farmers, coupled with weather data to inform them of the best time to harvest. In addition, you can choose your own geolocation and trip routing integrations for vehicle pathfinding.

## Solution idea: Choose crops

Co-operatives can aggregate and distribute data to their farmers in order to improve yields.

```diff
! A co-operative
+ can provide recommendations on the best crops to grow based on their market, geographic, and environmental patterns
- to decrease exposure to income loss and volatility by ~30%.
```

To implement this solution, you can use the starter kit to integrate with The Weather Company's data to track weather patterns and use the SMS gateway to provide recommendations to farmers on which crops would grow best in their region and climate. Your app would use a Cloudant database to store the data, you would use machine learning to analyze trends from weather data, and data on crop variation datasets and soil data projections, to provide recommendations for optimal product yields.

## Solution idea: Increase Prices

Farmers work with co-operatives to facilitate the buying and selling of their goods collectively.

```diff
! A co-operative
+ can find nearby markets to sell their products for the optimal price 
- to maximize profit by ~20–40%.
```

To implement this solution, you can use the SMS gateway integration provided by the starter kit to provide real-time messaging between farmers and cooperatives. You could create an API to gain access to buyers and markets by geolocation and use machine learning analyze the data to allow co-operatives to access local insights to determine competitive pricing and gain access to the market.  As a stretch goal, you might find and aggregate real-time price and market data, and optionally, integrate a distributed ledger, such as blockchain, to track transactions.
