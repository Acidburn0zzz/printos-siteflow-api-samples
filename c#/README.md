# C Sharp

## General Information

Code was written in Visual Studios 2015

NuGet package used

* Newtonsoft.json

Package restore should take care of this, but if something occurs and the package doesn't get restored. The version that was used is 9.0.1

## How To Run / Program Information

Program is a Console Application so F5 or clicking Start on the menu bar should build and run the program.

Before you can run the code, you need to provide the Key/Secret. There are two baseUrls provided. Uncomment the one that your Key/Secret was created/provided in.

The initial functions will validate the premade order. The premade order structure follows the structure documented [here](https://developers.hp.com/printos/doc/order-json-structure) 

Submitting an order will return information relating to it. See [../sample_output/submit_order_output.txt](https://github.com/HPInc/printos-siteflow-api-samples/blob/master/sample_output/submit_order_output.txt) to see the return information for a successful submission. Line 7 of the file is the id you pass into GetOrder(). To cancel one of the orders, you need the source account name (Line 241) and source order id (Line 234). The source order id is user generated. Having an order with an existing source order id will cause the validate and submit order to fail.

Note: The sample output is in python so the initial print statements will be different, but the structure of the JSON should be the same.