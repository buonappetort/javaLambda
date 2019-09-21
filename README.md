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
This tutorial was built using Eclipse - so we are assuming that you will be using #3, but you are free to follow the AWS Guide (https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/setup-install.html) for installing the dependencies using the other methods. 
</p>

<p>
Lesson learned -
While creating this doc, I attempted to retroactively package the java project - meaning I created it as a normal java project and then tried to import the aws dependencies. This proved to be a disaster - I then blew it away and restarted using the AWS toolkit for eclipse to create the package. This is the method that I recommend using. It makes life a lot easier
</p>

<p>
Start by installing the AWS toolkit for ecplise through the eclipse market place. While it is installing, make an IAM role for the lambda function to invoke and make sure the role has the correct permissions for lambda access. Once the Eclipse toolkit is installed then configure the access keys through the system preferences.
</p>

<p>Start a new "Java Lambda Project" using the AWS Toolkit in the toolbar.</p>

<p>
**INFo about the code
</p>

<p>
The code is going to be hosted in an S3 bucket, so we must have an S3 bucket created for it. The AWS toolkit will build the code for you into a zip file when you use the toolkit to push it to your S3 bucket. 
<br/>
Once the code is build and pushed to S3 you can test it by right clicking in the Eclipse window for the class and selecting "Run function on AWS Lambda". You can also test on the AWS Lambda console by creating a test configuration.
</p>









