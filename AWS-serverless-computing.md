# Serverless Computing Architecture

These are the services that we would be using from Amazon aws

![Serverless Computing](images/serverless.png "Serverless Computing")


![Architecture Diagram](images/architecture.png "Architecture Diagram")

* STEP1 1: How to create an API - Section 1 - Chapter 6

* STEP 2: How to create an API KEY - Section 3 - Chapter 19

     With the help of API KEY we can make sure that only with a valid key the API can be accessed. For each usage of API there are charges.      So always restrict the API with the help of key. You can also set usage plan for this API key. 
     
     You can also set that this API can be used only 1000 times per second. You can also set custom domains for your API. You can also set      log permissions for API usage

## Configuring Serverless

Install aws-cli and serverless globally

```
npm install -g aws-cli serverless
```

Then create a user in AWS and create a secret key and access key for the same user.

There are variety of cloud platforms that serverless can connect to like Google Cloud platform, AWS etc. To make serverless know what we need to use Amazon web services use the command below.

* username: serverless-admin
* Access Key: AKIAIMKE5NA4KOZEU44A
* Secret Key: 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
* shortform for serverless is sls

```
sls config credentials --provider aws --key AKIAIMKE5NA4KOZEU44A --secret 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 --profile serverless-admin
```
