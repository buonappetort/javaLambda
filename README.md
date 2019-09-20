# Lambda Functions

An introduction to lambda functions and a guide to implementing lambda functions in multiple languages.


## 1. Introduction

### What is AWS Lambda?

<p>
Lambda is a compute service offered by AWS (and competitors, but we'll cover other platforms in another article) that you can run without creating or managing servers. The code is only executed when you need it - and there is not charge for it when it is not running.
</p>
<p>The code is run in response to events - i.e. changes to data in an S3 bucket or an Amazon DynamoDB table, HTTP requests using API Gateway, or a number of other events. You can use lambda functions to build entire serverless applications deployed using codepipeline or codebuild (AWS services)</p>

## Java

<p>
Unlike Nodejs and Python - AWS Lambda functions authored in Java cannot solely be created using the console. The Java functions must be created locally and compiled to either a .jar or .zip file. We will go through both methods in this document. After compiling the file must be uploaded to AWS via the CLI or the console.
<br />
</p>

<p>
There are 3 ways by which you can import the Amazon SDK into your Java project

	1. Through Apache Maven
	2. Through Gradle
	3. Through the Eclipse Toolkit for AWS

<br />
This tutorial was built using Eclipse - so we are assuming that you will be using #3, but you are free to follow the [AWS Guide] (https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/setup-install.html) for installing the dependencies using the other methods.
</p>









