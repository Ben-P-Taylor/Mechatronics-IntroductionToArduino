# Calibrate Potentiometer Angle

## Introduction

The Aim of this exercise is to convert the ADC measurement value of the potentiometer voltage into an angle measurement, in degrees. The starting point for this exercise is the layout provided in <debugHL>[Building the Robot Document](./RobotBuild.md#LEDPatternBuild)</debugHL> and the <debugHL>[POT.ino](./Ex1ledPattern.md#potInoCode)</debugHL> example code provided at the end of <debugHL>[LED Pattern Exercise](./Ex1ledPattern.md)</debugHL>

!!! Info "GTA Marking"
    This is an assessed Exercise. When you have completed exercise, you should show your work to a GTA to get marked. 

!!! Note "Before Continuing"
    Before starting these exercises, you should ensure that you have completed the LED Pattern exercise and have the potentiometer and LED still connected. You should also read the <debugHL>[Analogue Sensors](./Background.md#analogue-sensors)</debugHL> section of the Background page. 
    
The following video is a quick demonstration of the final outcome from this exercise:

<figure>
<div style="text-align: center;">
<iframe id="kaltura_player" src='https://cdnapisec.kaltura.com/p/2103181/embedPlaykitJs/uiconf_id/53345422?iframeembed=true&amp;entry_id=1_a3eviyhm&amp;config%5Bprovider%5D=%7B%22widgetId%22%3A%221_4q6vxp1v%22%7D&amp;config%5Bplayback%5D=%7B%22startTime%22%3A0%7D'  style="width: 400px;height: 285px;border: 0;justify-content:center;" allowfullscreen webkitallowfullscreen mozAllowFullScreen allow="autoplay *; fullscreen *; encrypted-media *" sandbox="allow-downloads allow-forms allow-same-origin allow-scripts allow-top-navigation allow-pointer-lock allow-popups allow-modals allow-orientation-lock allow-popups-to-escape-sandbox allow-presentation allow-top-navigation-by-user-activation" title="Placeholder - Quick Test Video"></iframe>
</div>

<figcaption>Video demonstrating the expected outcome from this exercise</figcaption>
</figure>

## Exercise

The map function can be used to provide a linear calibration between a measured value and a real world parameter. In this exercise, you will use the ADC measurement value as the input to a `map()` function and use it to calculate the potentiometer angle.

!!! Info "`map()` function"
    See the `map()` function page from the Arduino language reference pages for a description: <debugHL>[https://docs.arduino.cc/language-reference/en/functions/math/map/](https://docs.arduino.cc/language-reference/en/functions/math/map/){target="_blank"}</debugHL>

**Procedure:**
 
1.	The starting point for this exercise is the Potentiometer test program, <debugHL>[POT.ini](./Ex1ledPattern.md#appendix-potino-code)</debugHL>, from the previous exercise and the LED pattern circuit from the <debugHL>[Building the Robot Document](./RobotBuild.md#LEDPatternBuild)</debugHL>.
2.	Add a map() function to the sketch to calibrate the potentiometer angle between -150 and 150 for an ADC measurement input of 0 to 1023.
3.	Using the Serial.print() and Serial.println() functions, (similar to that shown in <debugHL>POT.ino</debugHL>), write the data to the serial monitor with appropriate description.

!!! Info "Serial Communication Functions"
    See the serial communications functions page from the Arduino language reference pages for a description of the `Serial.print()` and `Serial.println()` functions: <debugHL>[https://www.arduino.cc/reference/en/language/functions/communication/serial/](https://www.arduino.cc/reference/en/language/functions/communication/serial/ "Link to the Arduino reference pages for the serial communications library")</debugHL>

**When completed, your code should function as follows:**

* When you rotate the potentiometer, the serial monitor should display the ADC read value and the potentiometer angle, in degrees.
* The serial monitor messages should provide a brief, (a word or 3), description of the variables printed and should be well formatted.
* The serial monitor should update at a reasonable rate – 2 to 4 times a second.

!!! Success "Now Get Your Work Marked by a GTA"
    Once you have completed your code and are satisfied with its operation, you should show your work to a GTA for marking.