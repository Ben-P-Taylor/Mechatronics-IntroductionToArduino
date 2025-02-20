# Introduction to Arduino Labs



!!! Danger "Danger: Read This First!"
    Before proceeding with further through this documentation or making any of the circuits discussed within, you must read the [**Disclaimer for using your personal Laptop or MacBook**](./Disclaimer.md).

!!! info "Before Starting the Exercises"
    Before starting the laboratory exercises, you should review the contents of the Mechatronics KIT Information folder, located in the Practicals content area of the Blackboard site for the Mechatronics course.

!!! Note "Note: Open This website on the computer you are programming your Arduino on"
    It is recommended that you open into website on the computer that you are doing your coding on, because there are several code examples that you can cut and paste directly from these documents into your working code.

## Introduction
During this activity you will have three laboratory sessions to complete a number of laboratory exercises, based around a simple mobile robotic chassis, as shown in <debugHL>[Fig. 1](#chassisPic)</debugHL>.

<figure  markdown="span">
  <a name="chassisPic"></a>
  ![Picture of the completed robot chassis.](./Images/Robot%201st%20Picture.jpg)
  <figcaption>Picture of the completed robot chassis.</figcaption>
  </figure>

## Aims and Objectives
The aims of these laboratory exercises are:

* To familiarize yourself with the Arduino Development Environment, IDE
* Gain experience of uploading user programs to the embedded target
* Provide you with hands-on experience of reading analogue sensor voltages into the Arduino device
* To convert these sensor values into meaningful measurement variables. 
* To drive different type of actuators using a PWM output from an Arduino device, 
* Use sensor information to adjust the behaviour of a system

To achieve these aims, the laboratory exercises are split into several assessed exercises, some are classed as basic and some advanced. A suggested timeline for achieving the **Basic** Exercises is provided in the <debugHL>[later in this section](#Timeline)</debugHL> of this documentation.

To acheiee the **Advanced** exercises you will need to put in extra effort, outside the laboratory sessions, to fulfil the requirements.

A list of the assessed exercises, with hyperlinks is provided:

- **Basic:** <debugHL>[LED Pattern](./Ex1ledPattern.md)</debugHL>
- **Basic:** <debugHL>[Calibration of Potentiometer Angle](./Ex2PotCalibration.md)</debugHL>
- **Basic:** <debugHL>[IR Sensor Measurement + Graph](./Ex3IrSensor.md)</debugHL>
- **Basic:** <debugHL>[Externally Powered Servo](./Ex4DriveServoMotor.md)</debugHL>
- **Basic:** <debugHL>[DC Motor](./Ex5DcMotor.md)</debugHL>
- **Basic:** <debugHL>[Encoders + Motor](./Ex6EncodeMotor.md)</debugHL>
- **Advanced:** <debugHL>[PI Control – Encoder Position](./Ex7PiEncoder.md)</debugHL>
- **Advanced:** <debugHL>[PI Control – IR Sensor Distance](./Ex8PiIrDist.md)</debugHL>
- **Advanced:** <debugHL>[PI Control – IR with Sequence](./Ex9PiIrSequence.md)</debugHL>

Each of these exercises will be assessed during the laboratory session, using the assessment structure outlined in the Appendix section of this document. When you have completed an assessed exercise, you should get your work marked one of the GTAs. 

!!! Warning
    **DO NOT leave all your exercises until the end of the 3rd laboratory session to get marked.** This may result in you running out of time to get your work marked within the allotted time, and you ***will*** lose marks. Instead, you should get your work marked as you complete each assessed exercise – see note below:

## Structure of Laboratory Sessions

The hardware kits that you will be using during these exercises are loaned to you for the duration of the Mechatronics module and you will take them home between laboratory and project sessions. 

!!! Note
    We will provide 3 supported laboratory sessions for you to work in, but you are also expected to do some work at home to ensure that you have completed all the exercises **AND** have them marked before the end of the 3rd laboratory session. 15 minutes before the end of the 3rd Introduction to Arduino laboratory session, we will stop marking work, with the remainder of the time being available for tidying your work area and exiting the laboratory. Any exercises not marked before this deadline, (regardless of whether they have been completed or not), will be forfeit and you will lose these marks. Please ensure that you get your work marked incrementally as you proceed through the exercises, and not leave them until the final moments, to avoid disappointment. 

    You can have any of the assessed exercises marked at any point during the three laboratory sessions, as long as there is someone free to mark your work.

## Suggested Timeline for your Work
<a name="Timeline"></a>
There is no rigid structure for your progress through these exercises, but the following time plan should be sufficient to ensure that you have time to complete all the exercises and have them marked by the GTAs before the end of the 3<sup>rd</sup> laboratory session.

### By the end of the 1<sup>st</sup> lab session
By the end of the 1<sup>st</sup> lab session, it is recommended that you have had the following exercises completed **and marked**:

* <debugHL><debugHL>[Constructed the Robot Chassis](./RobotBuild.md)</debugHL>
* **Basic:** <debugHL>[LED Pattern](./Ex1ledPattern.md)</debugHL>

### Before the start of the 2<sup>nd</sup> lab session
Before the start of the 2nd lab session, it is recommended that you have a working circuit capable of performing:

* **Basic:** <debugHL>[Calibration of Potentiometer Angle](./Ex2PotCalibration.md)</debugHL>

You should also ensure that you have read the exercise document, linked above. Ensure you have understood all the procedures.

### By the end of the 2<sup>nd</sup> lab session
By the end of the 2<sup>nd</sup> laboratory session, it is recommended that you have the following exercises completed **and marked**:

* **Basic:** <debugHL>[Calibration of Potentiometer Angle](./Ex2PotCalibration.md)</debugHL>
* **Basic:** <debugHL>[Externally Powered Servo](./Ex4DriveServoMotor.md)</debugHL>
* **Basic:** <debugHL>[DC Motor](./Ex5DcMotor.md)</debugHL>
 
### Before the start of the 3<sup>rd</sup> lab session
 
 Before the start of the 3<sup>rd</sup> lab session, it is recommended that you have a working circuit capable of performing:

* **Basic:** <debugHL>[Encoders + Motor](./Ex6EncodeMotor.md)</debugHL>

You should also ensure that you have read the exercise document, linked above. Ensure you have understood all the procedures.

###	By the end of the 3<sup>rd</sup> laboratory session

By the end of the 3<sup>rd</sup> laboratory session, ensure that you have **all exercises completed and marked.**

* **Basic:** <debugHL>[Encoders + Motor](./Ex6EncodeMotor.md)</debugHL>

!!! note
    To acheive the **Advanced** exercises you will need to put in extra effort, outside of the laboratory sessions, to fulfil the requirements, and work to your own timeline. The above time plan will only allow you to acheive the requirements for the basic exercises.