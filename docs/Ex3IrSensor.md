# Measure the Output of the Sharp IR Distance Sensor


Current stuff is not right
### Intro
### Circuit Setup
### Sensor Noise
### Experimental Setup with Lolly Stick up
### What Program to Write
### Expected Results
### Get your Work Marked

<debugHL>Merge some of the stuff from the the Calibrating IR sensor Document</debugHL>







## Introduction

The aim of this exercise is to generate a graph of sensor measurement from the Sharp IR distance sensor against measurement distance. During this exerercise, you will interface the Sharp IR distance sensor with the Arduino, record the measured voltage as a function of the distance to a target, and observe any constraints for the operation of this sensor.

!!! Info "GTA Marking"
    This is an assessed Exercise. When you have completed exercise, you should show your work to a GTA to get marked.

It should be noted:

* Noise
* Measurement characteristic


**Procedure:**

<problemHL>Check the Pinouts for this</problemHL>

1. The starting point for this exercise is the <debugHL>[circuit layout for the IR sensor](./RobotBuild.md#irSensor)</debugHL> and the potentiometer code, [POT.ini](./Ex1ledPattern.md#potInoCode), located at the end of the [LED pattern exercise](./Ex1ledPattern.md).

For more details on concerning the pin connections for the Sharp GP2Y0A21YK0F distance measurement sensor, see the data sheet for the sensor on the Blackboard site:

  * <debugHL>ACS231 Blackboards Site>>Mechatronics Kit Information>> Component Data Sheets and Technical Documentation.</debugHL>

<ol start=2>
  <li> Write an Arduino sketch to read the analogue measurement value from the IR distance sensor and display the reading on the serial monitor. (It is acceptable to use a fresh copy of the <debugHL><a href = ../Ex1ledPattern/#potInoCode>POT.ini</a></debugHL> as a template for this exercise.)</li>
</ol>

Once you have the measured value of the distance sensor being streamed to the serial monitor, you will be required to plot the distance sensor measurement value against distance measured, (with a ruler/scale).

During the development of this exercise, I briefly documented the setup I used to achieve this and have placed this document in the Blackboard for this laboratory. <problemHL>The Calibrating the IR sensor document</problemHL> contains several pointers for physical setup, software implementation and expected characteristic. 


<ol start=4>
  <li> Perform an experiment to characterise the Sharp IR sensor between 1cm and 80cm distance. The results from this experiment should be a graph of the ADC measurement value from the Sharp IR distance sensor, against the target distance. (See the Experimental Results section of the <problemHL>“Calibrating the IR sensor”</problemHL> document for a suggestion for distance point spacing).</li>
</ol>

You should plot your results in a computer package, such as Excel or MATLAB, with the x-axis as the distance measured, and the y-axis as the ADC measurement value. You must record the data values, because you will need them for <problemHL>Exercise 5.</problemHL>

I would recommend using a series of measurement points similar to:

1cm, 2cm, 3cm, 4cm, 5cm, 6cm, 7cm, 8cm, 9cm, 10cm, 15cm, 20cm, 25cm, 30cm, 35cm, 40cm, 45cm, 50cm, 55cm, 60cm, 65cm, 70cm, 75cm, and 80cm

(Note: on your plotted graph, you should include a title and axes labels for both the x-axis and the y-axis)

<strong>When completed, your code should allow you to run an experiment to draw the following graph:</strong>
<debugHL><ul><li><debugHL>A graph of ADC measurement value against distance.</debugHL></li>
<li><debugHL>The trace should be correctly framed within the axes.</debugHL></li>
<li><debugHL>Appropriate axes labels, with units and a descriptive graph title.</debugHL></li>
</ol>


!!! Success "Now Get Your Work Marked by a GTA"
    Once you have completed your code and are satisfied with its operation, you should show your work to a GTA for marking.

## Further Notes on experimental setup and Sensor Noise
