# Introduction to Arduino Labs



!!! Danger "Danger: Read This First!"
    Before proceeding any further through this documentation or making any of the circuits discussed within, you must read the <debugHL>[**Disclaimer for using your personal Laptop or MacBook**](./Disclaimer.md)<debugHL>.

!!! info "Before Starting the Exercises"
    Before starting the laboratory exercises, you should review the contents of the Mechatronics Kit Information folder, located in the Practicals content area of the Blackboard site for the Mechatronics course.

!!! Note "Note: Open this website on the computer you are programming your Arduino on"
    It is recommended that you open this website on the computer that you are doing your coding on, because there are several code examples that you can cut and paste directly from these documents into your working code.

## Learning Outcomes

By the end of these exercises you should be able to:

1. Use of basic hand tools to construct the mechanical and electrical systems of a simple mobile robot.
2. Program an Arduino to interface sensors and actuators and achieve a specified goal.
3. Integrate programs and concepts with sensors and actuators to create an operational mechatronic system.

## Introduction
During this activity you will have three laboratory sessions to complete a number of laboratory exercises, based around a simple mobile robotic system, as shown in <debugHL>[Fig. 1](#chassisPic)</debugHL>.

<figure  markdown="span">
  <a name="chassisPic"></a>
  ![Picture of the completed robot chassis.](./Images/Robot%201st%20Picture.jpg)
  <figcaption>Picture of the completed robot chassis.</figcaption>
  </figure>

## Website Layout
The Website is laid out in the following sections:

*  **This Introduction:** A quick overview of this section of the course, providing aims and objectives, structure of laboratory sessions, and a suggested timeline a subset of the assessed exercises.
*  <debugHL>[**Laptop Disclaimer:**](./Disclaimer.md)</debugHL> **You MUST read this disclaimer before continuing!**
*  <debugHL>[**Building the Robot Chassis Document:**](./RobotBuild.md)</debugHL> This page describes the building and recommended layout for the electronic circuit.
* <debugHL>[**Introductory and Supplementary Material:**](./IntroMaterial/README.md)</debugHL> There are two pages in this section:
    * <debugHL>[**Supplementary Signposting Document:**](./IntroMaterial/SupplSignPost.md)</debugHL> This document is aimed as a point of reference for students that are not confident with C or Arduino programming. The document provides reference links to external websites and the specific parts of the Arduino Language Reference pages, relating to elements of the Introductory exercises.
    * <debugHL>[**Introductory Exercises:**](./IntroMaterial/IntroExercises.md)</debugHL>This document provides you with two non-assessed exercises aimed at getting you started with installing and setting up the Arduino IDE, ready for use with these laboratory activities, and programming with simple I/O.
* <debugHL>[**Basic Exercises:**](./BasicExercises/README.md)</debugHL> This section provides five basic, assessed exercises aimed at reading sensors and driving actuators. These exercises are aimed at providing you with the scaffolding to for the more advanced integration exercises.
* <debugHL>[**Advanced Exercises:**](./AdvancedExercises/README.md)</debugHL> This section contains 3 advanced, assessed exercises, which require you to integrate the sensors and actuators learning from the basic exercises into simple mechatronics systems. During these exercises, we will introduce the programming of a PI controller and use a simple finite state machine. 
* <debugHL>[**Assessment Section:**](./Assessment.md)</debugHL> This section provides more details relating to the assessment and marking for all the exercises.

!!! Note
    You must have completed and have marked off all the basic exercises before you can receive credit for any of the advanced exercises.

## Aims and Objectives
The aims of these laboratory exercises are:

* To familiarize yourself with the Arduino Development Environment, IDE, and gain experience of uploading user programs to the embedded target
* Provide you with hands-on experience of reading analogue sensor voltages into the Arduino device and convert these into meaningful measurement variables. 
* To drive different type of actuators using a PWM output from an Arduino device, 
* Integrate sensors and actuators into a mechatronic system.

To achieve these aims, the laboratory exercises are split into several assessed exercises, some are classed as basic and some as advanced. A suggested timeline for achieving the <debugHL>[Basic Exercises](./BasicExercises/README.md)</debugHL> is provided in the <debugHL>[later in this section](#Timeline)</debugHL> of this documentation.

To achieve the <debugHL>[Advanced Exercises](./AdvancedExercises/README.md)</debugHL> you will need to put in extra effort, outside the laboratory sessions, to fulfil the requirements.

A list of the assessed exercises, with hyperlinks is provided:

- **Basic:** <debugHL>[LED Pattern](./BasicExercises/ledPattern.md)</debugHL>
- **Basic:** <debugHL>[IR Sensor Measurement + Graph](./BasicExercises/IrSensor.md)</debugHL>
- **Basic:** <debugHL>[Externally Powered Servo](./BasicExercises/DriveServoMotor.md)</debugHL>
- **Basic:** <debugHL>[DC Motor](./BasicExercises/DcMotor.md)</debugHL>
- **Basic:** <debugHL>[Encoders + Motor](./BasicExercises/EncodeMotor.md)</debugHL>
- **Advanced:** <debugHL>[PI Control – IR Sensor Distance](./AdvancedExercises/PiIrDist.md)</debugHL>
- **Advanced:** <debugHL>[PI Control – Encoder Position](./AdvancedExercises/PiEncoder.md)</debugHL>
- **Advanced:** <debugHL>[PI Control – IR with Sequence](./AdvancedExercises/PiIrSequence.md)</debugHL>

Each of these exercises will be assessed during the laboratory session, using the assessment structure outlined in the <debugHL>[**Assessment page**](./Assessment.md)</debugHL>  of this website. When you have completed an assessed exercise, you should get your work marked one of the GTAs. 

!!! Warning
    **DO NOT leave all your exercises until the end of the 3rd laboratory session to get marked.** This may result in you running out of time to get your work marked within the allotted time, and you ***will*** lose marks. Instead, you should get your work marked as you complete each assessed exercise – see note below:

## Structure of Laboratory Sessions

The hardware kits that you will be using during these exercises are loaned to you for the duration of the Mechatronics module and you will take them home between laboratory and project sessions. 

!!! Note
    We will provide 3 supported laboratory sessions for you to work in, but you are also expected to do some work at home to ensure that you have completed all the exercises **AND** have them marked before the end of the 3rd laboratory session. 15 minutes before the end of the 3rd Introduction to Arduino laboratory session, we will stop marking work, with the remainder of the time being available for tidying your work area and exiting the laboratory. Any exercises not marked before this deadline, (regardless of whether they have been completed or not), will be forfeit and you will lose these marks. Please ensure that you get your work marked incrementally as you proceed through the exercises, and not leave them until the final moments, to avoid disappointment. 

    You can have any of the assessed exercises marked at any point during the three laboratory sessions, as long as there is someone free to mark your work.

## Suggested Timeline for completing the Basic Exercises, only.
<a name="Timeline"></a>
There is no rigid structure for your progress through these exercises, but the following time plan should be sufficient to ensure that you have time to complete all the <debugHL>[Basic Exercises](./BasicExercises/README.md)</debugHL> exercises and have them marked by the GTAs before the end of the 3<sup>rd</sup> laboratory session. If you wish to complete the <debugHL>[Advanced Exercises](./AdvancedExercises/README.md)</debugHL>, you will need to create your own work plan, accordingly. 

### By the end of the 1<sup>st</sup> lab session
By the end of the 1<sup>st</sup> lab session, it is recommended that you have had the following exercises completed **and marked**:

* <debugHL><debugHL>[Constructed the Robot Chassis](./RobotBuild.md)</debugHL>
* **Basic:** <debugHL>[LED Pattern](./BasicExercises/ledPattern.md)</debugHL>

### Before the start of the 2<sup>nd</sup> lab session
Before the start of the 2nd lab session, it is recommended that you have a working circuit capable of performing:

* **Basic:** <problemHL>ReDoMe</problemHL>

You should also ensure that you have read the exercise document, linked above. Ensure you have understood all the procedures.

### By the end of the 2<sup>nd</sup> lab session
By the end of the 2<sup>nd</sup> laboratory session, it is recommended that you have the following exercises completed **and marked**:

* **Basic:** <problemHL>ReDoMe</problemHL>
* **Basic:** <debugHL>[Externally Powered Servo](./BasicExercises/DriveServoMotor.md)</debugHL>
* **Basic:** <debugHL>[DC Motor](./BasicExercises/DcMotor.md)</debugHL>
 
### Before the start of the 3<sup>rd</sup> lab session
 
 Before the start of the 3<sup>rd</sup> lab session, it is recommended that you have a working circuit capable of performing:

* **Basic:** <debugHL>[Encoders + Motor](./BasicExercises/EncodeMotor.md)</debugHL>

You should also ensure that you have read the exercise document, linked above. Ensure you have understood all the procedures.

###	By the end of the 3<sup>rd</sup> laboratory session

By the end of the 3<sup>rd</sup> laboratory session, ensure that you have **all exercises completed and marked.**

* **Basic:** <debugHL>[Encoders + Motor](./BasicExercises/EncodeMotor.md)</debugHL>

!!! note
    To acheive the **<debugHL>[Advanced Exercises](./AdvancedExercises/README.md)</debugHL>** exercises you will need to put in extra effort, outside the laboratory sessions, to fulfil the requirements, and work to your own timeline. The above time plan will only allow you to acheive the requirements for the basic exercises.