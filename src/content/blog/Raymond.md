---
author: Samuel Chandler
pubDatetime: 2024-08-24T00:39:58Z
title: My Time At The Raymond Corporation
slug: Raymond
featured: true
draft: false
tags:
  - experience
  - Software
  - Electrical
  - Manufacturing
description:
  A Post about my time at The Raymond Corporation during the Summer and Fall of 2023
---

## Table of contents

# The Raymond Corporation

![RayLogo](assets/images/RayLogo.png)
During my Spring 2023 semester I was extended the opportunity to work within the Product Engineering Team as a coop for a seven month period during the summer and fall sessions of 2023 at Greene NY. 

Upon considering the offer, I accepted with excitement to learn what it means to be a professional engineer and to work in a competitive environment. And The Raymond Corporation, one of the largest producer of electric lift trucks and supply chain solutions, did not disappoint. 

# Product Engineering

Within The Raymond Corporation, I worked in the Product Engineering team which worked to source alternative components for released trucks in the case of obsolescence or shortages in our supply chain. In addition, we would also work to make improvements to the released models for cost savings or for new safety standards or production methods that we are implementing in manufacturing. 

My job as a Co-op was to assist in these activities and to help the other employees within the department for these activities. This would usually involve performing testing, sourcing alternatives for older components, updating documentation, and also documenting new processes. 

# Projects

During my time at Raymond I got to work on multiple really interesting projects including the regular work I was doing to assist other team members with testing and finding alternative options for obsolescent parts. 

These range from developing trainings for PLC's, Developing a Python application for interpreting CAN messages, and Finishing up a Test fixture For testing cables that we want to validate.

## PLC Trainings

A Programmable Logic Controller (PLC) is a tool that was used throughout Raymond to create testing environments and in some of our models due to the ease of programming, high reliability, and diagnostic capabilities. 

Before my time at Raymond a previous intern worked on a control box that would be used for testing and as a learning tools for new employee onboarding. When trying to work with them however, I found that there were multiple issues I ran into in setting up the environment and found a abandoned task for creating learning modules for the create PLC training boxes.

I decided that the creation of these learning labs for the test boxes would be worth the time and would speed up the learning process for future employees. 

With this in mind I created 2 labs for the Direct Soft 6 Suite of PLC's.

![directSoft6](assets/images/ds6.jpg)

### Lab 1, Basic Input Output

For the first Lab I focused on detailing how to send and receive signals too and from the PLC as well how to set up the PLC using Direct Soft 6.

This was pretty simple with the exclusion of making sure to properly detail the set up of the software to prevent any forseeable issues. 

The end result of the lab would be a basic device that would light up a certain color based on the button pressed using the PLC's relays and some basic ladder logic (the method you program the PLC's Logic)

### Lab 2, A Focus on Ladder Logic and Control Blocks

For the second lab I decided to go into a bit more detail on how information is stored within the PLC by creating directions to create a binary counter with the 3 lights that were used in the previous lab. 

The general Idea for the end product was to create a binary counter that would increase when a button was pressed and reset at its max value or when a second button was pressed.

This would ideally teach the concept of how information was stored within the PLC's through the use of registers and how there could be used and accessed through the use of control blocks to add or subtract from the current total displaying the result as a binary number through the Lights of the training box. 

## Cable Test Fixture

After completing the training documentation on the PLC's I then got to work on completing the test fixture that was initially created by a previous intern. 

The Fixture itself was designed to test the long term capabilities of cables we were going to use in production by applying torque to 8 cable samples through a motor that would twist the cables. The PLC would then detect when the internal of the cable would become open and alert the user and stop the count giving the amount of cycles the cable could withstand before breaking.

The initial state of the fixture when I received was a bit worse for ware, as it was built atop a wooden plank and the connections were hand soldered for each cable. However it was in a functioning state and was able to correctly stop and detect openings in the cable.

### Improvements

The first thing I did when I received the fixture was to move it to a proper case that would contain the PLC and components needed to keep the fixture running and to prevent any outside interference when possible. This also involved my cleaning up cable lengths. 

The power supply for the fixture was also using a variable power supply which was a bit bulky and used a recourse that we would often need for other testing. I went ahead and sourced a 24 power supply to replace this and added a buck converter to lower the voltage for the motor controller to use at 5V. 

One of the final improvements that I made to the fixture was adding terminal blocks to the ring of the cables to allow the easy replacement of the cables so we wouldn't have to hand solder each cable when one would be replaced which was mainly done out of convenience for setup and teardown. 

### Testing 

After the improvements made to the fixture, I was able to start a trial run of the fixture leaving it to run for about a month to test if the fixture would break before the cables would. 

Unfortunately nothing stopped working with the exclusion of power outages that would take place and even then the PLC kept track of the readings and you could start the process from where it left off. 

Even on my last day nothing broke and I still believe that the fixture is running somewhere at Raymond.

## CAN Message Translator

The Final Project that I got to work on was a CAN translation python script that would take the resulting file from a tracing using a P-CAN device and find the value of each field being transmitted throughout the truck by taking the CAN frame and translating each value within it. 

![PCAN_Device](assets/images/PCAN.jpg)

This was done by taking the output of the P-CAN Device (an 8 byte code) and the Node ID of the message, splitting and translating the output based on the given Node ID. 

The basic architecture for the script was to create a python class for each of the Node ID's in the output. Each class containing the methods for separating the output of the message into given fields and then translating each of those fields from a binary format into a readable format such translating a 4 byte binary value into Rotations Per Minute, MPH, or detailing the certain state of a device connected to the CAN Line. 

The results of the translations would then be saved as a formatted xlsx file that could be shared within the business. 

Also during this time I was able to make a basic UI for the application as well as creating documentation on how to use the CLI version of the tool. 

# Conclusion

The Raymond Corporation, was an excellent place to work and grow professionally and through working on a wide range of projects as well as assisting in the day to day operations of the company I feel looking back that Raymond had provided a place where I could really become a Engineer, learning multiple skills both technical and professional. 





