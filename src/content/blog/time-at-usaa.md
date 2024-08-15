---
author: Samuel Chandler
pubDatetime: 2024-08-15T19:22:00Z
title: My Time At USAA 
slug: time-at-usaa
featured: true
draft: false
tags:
  - Employment
  - experience
  - Software
  - Web
description:
  A Post about my Time at USAA and what I worked on during my time there.
---

![USAA_Logo](assets/images/USAA-logo.png)

## Table of contents

## My Role and Team
Within my time at USAA, I worked within the Bill Pay department which was responsible for the method for which are members paid for their bills within USAA's Web and Mobile interfaces. 

My Role Within this team was mainly to create Integration Tests for the new endpoints we were developing during the sprints that took place during my time at USAA.

## Postman And Integration Testing 

![USAA_Logo](assets/images/Postman-Logo.png)

For Integration Testing my role was designing the initial test that would be performed for the endpoints being created to verify the functionality of these endpoints in the future. 

Through this experience I got to write a variety of tests for the multiple variations of endpoints and test the returning information to verify that it met with the original parameters for the approved endpoint we planned to create. Communicating when there were any differences between the plan compared to what I was getting to confirm the desired functionality. 

Postman was a tool I quickly learned to use for creating repeatable tests and to set the environment for the tests to occur in so that I could easily communicate issues with the team and verify a wide range of information through the Pre and Post request scripts that I could create using JavaScript to automate the verification process.

## Special Intern Project With Generative AI 

![AmazonBedrockLogo](assets/images/AmazonBedrockLogo.webp)

One of the most interesting projects I had the opportunity to work on was a new application that used AWS tools to allow for the quick creation of documentation for features and the relating information such as stories, boilerplate code, diagrams, and feature documentation. 

This feature was made in a team of 4 including myself and was presented in front of the CIO of USAA's bank department this summer.

My personal contribution to the project was in the feature level details that would be created and the diagrams created through Amazon Bedrock. This means that I was  designing the information that would be passed to the generative AI model through a practice called Prompt Engineering. A field I didn't realize existed before working on this project. 

One of the most interesting part of the project from my experience was working with Amazon Step Function and the use of Bedrock to create diagrams using Mermaid.

### Amazon Step Functions
![AmazonStepFunctionLogo](assets/images/StepFunctionLogo.jpg)

One of the most interesting things I got to learn about through this project was how to use AWS Step Functions to orchestrate calls to AWS bedrock and to forward information from that to AWS Lambda calls which could then be used to format another query into AWS Bedrock. 

This was the most important tool that we were using in the feature we created as it allowed us to chain queries into the ai into formatting and then creating a new query with a lambda using the information from the first. All of this and we could also record the results of each step into an S3 bucket to look back on later.  

This was definitely an interesting tool to use and I look forward to finding new and unique ways in which I could use this in the future. 

### Mermaid

Mermaid is also a really interesting technology I got to use for this project where I got the format a text output that could be used to create a diagram. 

Lets Look at an example of what I mean. 
#### Code
```
sequenceDiagram
    Alice ->> Bob: Hello Bob, how are you?
    Bob-->>John: How about you John?
    Bob--x Alice: I am good thanks!
    Bob-x John: I am good thanks!
    Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

    Bob-->Alice: Checking with John...
    Alice->John: Yes... John, how are you?
```

#### Resulting Diagram
![mermaidSD](assets/images/MermaidResult.png)

Using Prompt Engineering and through the Use of Mermaid we can now create visual assets through text! 

This was what I ended up spending the most time working on and eventually got the formatting to a consistent place where I would get a correct mermaid diagram every time I would prompt the AI to create a new diagram using the resulting information of the previous response after formatting it through a lambda. 

## Conclusion 
Overall My Time at USAA was a interesting and educational for me, as I got to try out technology I would of never tried before within the corporate environment. And I'm sure that I will look back on this experience fondly in the future.