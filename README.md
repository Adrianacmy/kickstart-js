# IRCO Class Notifier
Created By Mary Anne Thygesen, Anna Spysz, Claire Flanagan, Adrianna Chen, Sarah Steinberg and Ben Kiggen.

## About the App

This app was created in ~6 hours as part of the WeCode2018 Hackathon. The participants contributed as follows: 

* Mary Anne - Team Leader
* Sarah - Front-end
* Claire - Front-end
* Ben - Front-end
* Anna - Back-end

![Screenshot](client/public/screenShot.png?raw=true "Title")

### Problem:

IRCO offers hundreds of different programs to thousands of immigrants and refugees throughout the northwest Oregon and southwest Washington region. With such a wide variety of programming, keeping track of upcoming events can be a challenge for participants.

### Solution:

Starting with the SUN school program, we created a text notification app where families can sign up to receive reminders about upcoming after-school classes. With a very simple UI, users are able to easily add their phone number, select their school, and opt in to reminders about their chosen programs. Using the To Google Translate Firefox extension, users can translate messages into their language of choice. This app could potentially be expanded to deliver reminders to participants in the various other IRCO programs.


## Technologies Used

* React
* AWS CloudFormation
* AWS Lambda 
* DynamoDB
* SNS (Simple Notification Service)

* The backend will need to be deployed within IRCO's AWS Account using CloudFormation

## Getting Started - front-end

  1. Download the .zip file or clone from the command line
  2. Run ``` npm install ```
  3. Then run ``` npm run start ```

## Getting Started - back-end

  1. Clone the back-end repo: https://github.com/bildungsroman/irco-backend
  2. The `template.yaml` file is an AWS SAM serverless template. It needs to be deployed to AWS CloudFormation using either the AWS Console or the AWS CLI:
     1. 
    ```bash
    $ aws cloudformation package \
    --template-file /path_to_template/template.yaml \
    --s3-bucket bucket-name \
    --output-template-file packaged-template.yaml
    ```
     1. Docs: https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-deploying.html 

## Legal
Copyright 2019
MIT License

