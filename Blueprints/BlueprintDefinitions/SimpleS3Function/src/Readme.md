# AWS Lambda Simple S3 Function Project

This starter project consists of:
* Function.cs - class file containing a class with a single function handler method
* aws-lambda-tools-defaults.json - default argument settings for use with Visual Studio and command line deployment tools for AWS
* project.json - .NET Core project file with build and tool declarations for the Amazon.Lambda.Tools Nuget package

You may also have a test project depending on the options selected.

The generated function handler responds to events on an Amazon S3 bucket. The handler receives the buckey and object key details in a S3Event instance and returns the content type of the object as the function output. Replace the body of this method, and parameters, to suit your needs.

After deploying your function you must configure an Amazon S3 bucket as an event source to trigger your Lambda function.

## Here are some steps to follow from Visual Studio:

To deploy your function to AWS Lambda, right click the project in Solution Explorer and select *Publish to AWS Lambda*.

To view your deployed function open its Function View window by double-clicking the function name shown beneath the AWS Lambda node in the AWS Explorer tree.

To perform testing against your deployed function use the Test Invoke tab in the opened Function View window.

To configure event sources for your deployed function, for example to have your function invoked when an object is created in an Amazon S3 bucket, use the Event Sources tab in the opened Function View window.

To update the runtime configuration of your deployed function use the Configuration tab in the opened Function View window.

To view execution logs of invocations of your function use the Logs tab in the opened Function View window.

## Here are some steps to follow to get started from the command line:

Once you have edited your function you can use the following command lines to build, test and deploy your function to AWS Lambda from the command line (these examples assume the project name is *SimpleS3Function*):

Restore dependencies
```
    cd "SimpleS3Function"
    dotnet restore
```

Execute unit tests
```
    cd "SimpleS3Function/test/SimpleS3Function.Tests"
    dotnet test
```

Deploy function to AWS Lambda
```
    cd "SimpleS3Function/src/SimpleS3Function"
    dotnet lambda deploy-function
```
