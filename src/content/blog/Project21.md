---
author: Samuel Chandler
pubDatetime: 2024-08-16T18:56:25Z
modDatetime: 2024-08-17T21:28:47Z
title: Project 21cm
slug: Project21
featured: true
draft: false
tags:
  - School
  - experience
  - Software
  - RF
  - Electrical
description:
  A Post about my Senior Design Project 21cm and what I worked on during that semester
---

## Table of contents

# Senior Design 1
During my time at the University of Texas at Dallas during the spring semester I had the opportunity to lead a team of talented individuals to create the design for our senior project
that we would build during the following fall semester. 

This ended up being a very educational experience about what it means to fully plan out a project and presenting that plan under the scrutiny of other engineers within the field.

I was very lucky to have had the opportunity to lead a team of 4 in creating A project that I believe to be very interesting and not something that is typically though of.

# The Initial Idea

After having multiple brainstorming sessions within the team, we determined that the project that we would make was a Radio Telescope that we could use to create an image of the stars. 

We determined this was the best choice for multiple reasons. 
1. Designing an antenna seemed like a very interesting experience that none of us had done before. 
2. Creating an image from the resulting scan would present really well and could easily measure the successfulness of the project. 
3. RF was not very explored in our coursework and we saw it as a way to learn something new. 
4. As the Rest of the team was electrical engineers it seemed like a programming light project to take on (This ended up being incorrect)

With these reasons in mind we determined that for our Senior Design we would aim to create a telescope that could detect the hydrogen line and record its intensity into an image. 

# The Hydrogen Line

For the sake of time, I wont go into to much detail on what the hydrogen line is and will instead point you [Here](https://en.wikipedia.org/wiki/Hydrogen_line)

But in the context of this project explanation, all you really need to know is that hydrogen will occasionally release a frequency at 1.42 GHz or 21 cm wavelength (get it) and when the entirety of the universe is made up of hydrogen, this signal is very common and varies in magnitude.

# Project Goal

With the hydrogen Line in mind we now have to determine what our goals for the project will be

Based on what we wanted to create we determined that we wanted the following functionality for the device. 
- Detect 1.42 GHz signals given off by hydrogen 
- Create An Image of those signals based on the location and magnitude of the signal 
- Create the device to be below $1000 in components 

With this in mind we then went to designing the 4 Subsystems that would make up this device. The Antenna, Signal Processing, Mounting Solution, and The program that will create the resulting image.

# The Device 
![HornAttenaEx](assets/images/PosterDiagram.png)

## Antenna
![HornAttenaEx](assets/images/hydrogenline_horn.jpg)
^ example of a similar horn antenna

The Antenna Design we ended up going with was a horn antenna that we designed to capture 1.42 GHz and to also have the gain characteristics to detect the differences at multiple positions. Our reasoning for this form factor was relatively simple, Manufacturing.

 With the means we had creating an antenna was already a difficult task and enable to make it achievable we determined the best course of action to be designing a antenna devoid of any difficult curves, instead opting for straight angles.

 ## Signal Processing 

![SDR](assets/images/h1.jpeg)

 Once we receive a signal we need to determine a way to format that signal into a digital format. 

 This is the role of the SDR we have decided to use for this design, the HackRF One. 

 This device will enable us to quickly take readings from the antenna getting the magnitude of the signal being received at 1.42 Ghz and then sending that reading to our recording program. 


## Mounting System 

For the mounting system for the antenna we had 3 goals in mind. 
1. Needs to be able to traverse azimuth
2. Needs to be able to traverse elevation
3. Needs to be able to communicate its current position

With that in mind we determined that a 2 motor system would work best where each motor controls a range of motion. 

The first Motor would change the azimuth of the device by rotating the other motor and antenna which will be placed atop a spinning plate. 

The second motor would be placed next to the antenna and will control the elevation of the antenna and hold it in place when traversing the azimuth when scanning 

The Final piece the the mounting system will be the motor controllers themselves which we plan on using to communicate the position of the antenna to the personal device of the user 
device for the sake of creating the image.

## Programming

The Program itself can be split into two separate systems the first is the recording process that will take the magnitude of the signal and store that result with the location of the antenna given by the motor controller.

The Second is the script for the image creation itself taking the recorded information and creating an image from that information once fully collected. 

### Recording Process 

![MotorControl](assets/images/MotorControllerCommunication.png)

Above is the current plan we developed for recording the position of the antenna in between recording the signals magnitude through the SDR.

The measurements will upon completing the recording be saved into a xlsx file that we will then use to create an image using the Image process explained in later. 

### Image Creation

![ImageCreationProccess](assets/images/Conversion_Process.png)

The process detailed can essentially be boiled down into 3 steps for simplicity 
1. Scale the Magnitude or the Readings to Be Relative to each other and to detect outliers from the other readings. 
2. Use The Location of the reading to map that magnitude to the image
3. Create and store the resulting image to the personal device of the user

With this image we can quantify the successfulness based on the requirements we initially created. In Addition we are also now able to share cool photo's of the hydrogen line to others!

# Conclusion

With this idea and plan we were able to present the idea during our senior design expo during Spring 2024 and get feedback on our design by many engineers that are currently in industry and we look forward to constructing the device during this fall semester. 