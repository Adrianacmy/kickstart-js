# IRCO Class Notifier
Created By Mary Anne Thygesen, Anna Spysz, Claire Flanagan, Adrianna Chen, Sarah Steinberg and Ben Kiggen.

## About the App

This app was created in ~6 hours as part of the WeCode2018 Hackathon. The participants contributed as follows: 

* Mary Anne - Team Leader
* Sarah - Front-end/Form functionality
* Claire - Front-end/Design
* Ben - Front-end/Design
* Adrianna - Front-end/React
* Anna - Back-end

![Screenshot](client/public/screenShot2.png?raw=true "Title")

### Problem:

IRCO offers hundreds of different programs to thousands of immigrants and refugees throughout the northwest Oregon and southwest Washington region. With such a wide variety of programming, keeping track of upcoming events can be a challenge for participants.

### Solution:

Starting with the SUN school program, we created a text notification app where families can sign up to receive reminders about upcoming after-school classes. With a very simple UI, users are able to easily add their phone number, select their school, and opt in to reminders about their chosen programs. Using the To Google Translate Firefox extension, users can translate messages into their language of choice. This app could potentially be expanded to deliver reminders to participants in the various other IRCO programs.

### Target:

This app would allow parents of children participating in SUN classes to sign up and receive text notifications reminding them of their children's schedule, as well as adults in the adult classes. The text message format is accessible to anyone with any kind of mobile phone, allowing those without smartphones to participate as well.

For the purposes of security and privacy, the app does not collect user information such as name or location, just phone number.

#### To Do:

1. Fix SNS topic functionality
2. Add functionality to `src/sendScheduledMessage` to process events added to the `phoneData` table and set up additional SNS topics that regularly message users

## Technologies Used

* **React** (front-end)
* **AWS CloudFormation** (back-end)
* **AWS Lambda** (back-end logic)
* **AWS DynamoDB** (database for form data storage)
* **AWS SNS** (Simple Notification Service) (sends text messages to users)
* _The backend will need to be deployed into IRCO's AWS Account using CloudFormation_

## Getting Started - front-end

  1. Download the .zip file or clone from the command line
  2. Run ``` npm install ```
  3. `cd` to the `client\` directory
  4. Run ``` npm install ```
  5. Then run ``` npm run start ```

## Getting Started - back-end

  1. Clone the back-end repo: https://github.com/bildungsroman/irco-backend
  2. The `template.yaml` file is an AWS SAM serverless template. It needs to be deployed to AWS CloudFormation using either the AWS Console or the AWS CLI:

```bash
    $ aws cloudformation package \
    --template-file /path_to_template/template.yaml \
    --s3-bucket bucket-name \
    --output-template-file packaged-template.yaml
```

  3. AWS Docs on deploying: https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-deploying.html 

## Legal
Copyright 2019
MIT License

