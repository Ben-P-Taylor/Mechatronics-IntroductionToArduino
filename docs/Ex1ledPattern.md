## Introduction

During the LED Pattern exercise you will generate a repeating sequence on 3 LEDs, use a potentiometer to change the cycle rate of the sequence, and use a push button to pause the sequence.

!!! info "GTA Marking"
    This is an assessed Exercise. When you have completed part 3, you should show your work to a GTA to get marked.
    

!!! Note
    Before starting these exercises, you should ensure that you have added the LEDs, the button and the potentiometer to the breadboards on the robot chassis, as suggested on <debugHL>[Building the Robot: Fig. 6](./RobotBuild.md#BreadboardComps)</debugHL>. Furthermore, you should ensure that your connections for these components are correct - suggested connections are shown in <debugHL>[Building the Robot: Table. 1](./RobotBuild.md#ArduinoConnect)</debugHL>.

<problemHL>Can We get a Tinker CAD Drawing of the LED, Potentiometer and Button Corcuit on Breadboards</problemHL>

The following video is a quick demonstration of the final outcome from this exercise:

<figure>
<div style="text-align: center;">
<iframe id="kaltura_player" src='https://cdnapisec.kaltura.com/p/2103181/embedPlaykitJs/uiconf_id/53345422?iframeembed=true&amp;entry_id=1_a3eviyhm&amp;config%5Bprovider%5D=%7B%22widgetId%22%3A%221_4q6vxp1v%22%7D&amp;config%5Bplayback%5D=%7B%22startTime%22%3A0%7D'  style="width: 400px;height: 285px;border: 0;justify-content:center;" allowfullscreen webkitallowfullscreen mozAllowFullScreen allow="autoplay *; fullscreen *; encrypted-media *" sandbox="allow-downloads allow-forms allow-same-origin allow-scripts allow-top-navigation allow-pointer-lock allow-popups allow-modals allow-orientation-lock allow-popups-to-escape-sandbox allow-presentation allow-top-navigation-by-user-activation" title="Placeholder - Quick Test Video"></iframe>
</div>
<figcaption>Video demonstrating the expected outcome from this exercise</figcaption>
</figure>
## Part 1: LED Sequence
<a name="Part1"></a>
During this part, you will write a program to create a repeating sequence of LEDs, with a fixed sequence time step, e.g. say every ½ second. A suggested LED sequence is shown in <debugHL>[Table. 1](#ArduinoConnect)</debugHL>. 

<table>
  <a name="ArduinoConnect"></a>
  <thead>
    <tr> <th>Sequence Index:</th> <th>LED 3 (DIO 13)</th> <th>LED 2 (DIO 12):</th> <th>LED 1 (DIO 11):</th> </tr>
  </thead>
  <tbody>
    <tr> <td>0</td><td>0</td><td>0</td><td>0</td> </tr>    
    <tr> <td>1</td><td>0</td><td>0</td><td>1</td> </tr>    
    <tr> <td>2</td><td>0</td><td>1</td><td>0</td> </tr>    
    <tr> <td>3</td><td>0</td><td>1</td><td>1</td> </tr>    
    <tr> <td>4</td><td>1</td><td>0</td><td>0</td> </tr>    
    <tr> <td>5</td><td>1</td><td>0</td><td>1</td> </tr>    
    <tr> <td>6</td><td>1</td><td>1</td><td>0</td> </tr>    
    <tr> <td>7</td><td>1</td><td>1</td><td>1</td> </tr>    
  
  </tbody>
  <caption>Suggested simple repeating sequence, (counting-up in binary).</caption>
</table>

We will not provide any example code to facilitate this exercise, you must create this code from scratch, possibly using some of the example code provided in the <debugHL>[Introductory Exercises](./IntroExercises.md#buttCode)</debugHL> or the built-in examples as inspiration.

**Procedure:**

1. Ensure that the circuit is correctly connected:
    * We suggest the anode of the LED be connected to Arduino pins DIO11 to 13.
    * Each of the cathodes of the LEDs should be connected through a 470Ω resistor to ground.
2. Write a program to change the pattern of the LEDs at a fixed rate, say every ½ second, and loop through the sequence continuously. We suggest using the sequence from <debugHL>[Table 1](#ArduinoConnect)</debugHL>.
3. If you do not use the sequence provided in <debugHL>[Table 1](#ArduinoConnect)</debugHL>, your sequence should have at least 8 patterns, some but not most may repeat.
4. For this we suggest using a delay function to control the timing of the sequence. The rationale for this is that we will replace the bracket value on the `delay()` function with the ADC read value, to control the speed of the sequence. 
5. Ensure that you save your code when you have completed this part.

!!! Note 
    We strongly recommend using the suggested connection and layout provided in <debugHL>[Building the Robot Document](./RobotBuild.md#LEDPatternBuild)</debugHL> because it will link conveniently with the discussions and the example code provided. Using the suggested layout and connections also makes debugging your work easier because you will have a more familiar structure for the staff and GTAs.

## Part 2: Potentiometer Control of the Sequence Rate

!!! info
    It is suggested in the <debugHL>[Building the Robot Document](./RobotBuild.md#LEDPatternBuild)</debugHL> that your potentiometer is connected to analogue pin A5.

This part of the exercise is split into two sub sections:

1. Using the <debugHL>[POT.ino](#potInoCode)</debugHL> test program to read the potentiometer value and display it on the serial monitor.
2. Modifying the LED sequence code so that the potentiometer value is used to control the pattern change rate of the LED sequence.

### Section 1: The Read the Potentiometer Test Program, POT.ino
The aim of the <debugHL>[POT.ino](#potInoCode)</debugHL> example code is to show you how to read an analogue value from a sensor, or other device, and use its value. In this example code you will read the voltage from a potentiometer, generate a PWM output to change the brightness of an LED, and stream some data to the Serial Monitor. 

**Procedure:**

1. Copy the <debugHL>[POT.ino](#potInoCode)</debugHL> code into a black Arduino sketch and save it into your working folder.
2. Ensure the LEDs and potentiometer are connected into your circuit, as described in the <debugHL>[Building the Robot Document](./RobotBuild.md#LEDPatternBuild)</debugHL>
3. Ensure the potentiometer is connected into the circuit.
    * Connect left hand pin of the potentiometer to GND and the 5V and the right hand pin to +5V.
    * It is suggested that the middle pin of the potentiometer is connected to the analogue A5 pin.

The analogue to digital converter, ADC, inputs to the Arduino have 10 bits of resolution (i.e. 1024 different values). By default, they measure from ground (0V) to 5 volts. That means that the 0-5V range of the potentiometer will be proportionally mapped to the 0-1023 digital values range in the microcontroller. 

<ol start=4>
  <li>Upload the program to the Arduino, then open the serial monitor and observe data being streamed to the terminal.</li>
  <li>Rotate the knob of the potentiometer and observe the range that the data spans.</li>
  <li>Observe the rightness of the LED as you rotate the potentiometer.</li>
  <li>Ensure that you save your code when you have completed this section.</li>
</ol>

This example program uses the map() function to ‘map’ the ADC measurement values between 0 and 1023, to a range of 0 to 255. This new range is required to write the PWM signal to change the LED brightness – PWM will be covered in the next lab session, so for this example, just assume this is an analogue output from the Arduino.

Look at the code and see how the map() command is used. The Arduino language reference for the map command can be found at:

<debugHL>[https://www.arduino.cc/reference/en/language/functions/math/map/](https://www.arduino.cc/reference/en/language/functions/math/map/ "Map command in the Arduino reference documentation")</debugHL> 

### Section 2: Integrate the Potentiometer Value Into Your LED Sequence Program
During this section you will integrate the reading of the potentiometer into the program for your LED sequence, and use the ADC value to control the delay function in the main loop.

**Procedure:**

1. Starting with the code you wrote in <debugHL>[Part 1](#part-1-led-sequence)</debugHL>, modify your code to read the voltage value of the potentiometer, using the ADC, each time the sequence value changes.
2. The ADC value should be used to control the `delay()` function time within the sequence loop.
3. Ensure that you save your code when you have completed this section.

When you rotate the potentiometer to the right, the sequence should speed up, and when you rotate the potentiometer to the left, the sequence should slow down. There should be a continuous variation in sequence speed proportional to the position of the potentiometer between the left and right extremes.

## Part 3: Addition of a Pause Button
During this part, you will implement the reading of the button on breadboard 1 and use the button value to pause the execution of the sequence.

**Procedure:**

1. Starting from your code that you completed in <debugHL>[Part 2, section 2](#section-2-integrate-the-potentiometer-value-into-your-led-sequence-program)</debugHL>, implement a button read from the button on breadboard 1.
2. Use this the pressed value of the button to hold the flow of execution until the button is released. 

**When completed, your code should function as follows:**

* The three LEDs should be flashing in a continuously repeating sequence of at lease 8 different patterns.
* When you rotate the potentiometer to the right, the sequence should speed up, and when you rotate the potentiometer to the left, the sequence should slow down. There should be a continuous variation in sequence speed proportional to the position of the potentiometer between the left and right extremes.
* When the button is pressed, the sequence should pause, but not reset.


!!! Success "Now Get Your Work Marked by a GTA"
    Once you have completed your code and are satisfied with its operation, you should show your work to a GTA for marking.

## Appendix: POT.INO Code

<a name="potInoCode"></a>

``` Arduino title="POT.ino Arduino Code"
// Global Name Space
int potAnalogPin = 0; // FSR is connected to analog 0
int LEDpin = 11;      // connect Red LED to pin 11 (PWM pin)
int potReading;      // the analog reading from the FSR resistor divider
int LEDbrightness;
 
void setup(void) {
  // We'll send debugging information via the serial monitor
  Serial.begin(9600);   
  pinMode(LEDpin, OUTPUT);
}
 
void loop(void) {
  potReading = analogRead(potAnalogPin);
  Serial.print("Analog reading = ");
  Serial.println(potReading);
 
  // we'll need to change the range from the analog reading (0-1023) down to
  //the range used by analogWrite (0-255) with map!
  LEDbrightness = map(potReading*1, 0, 1023, 0, 255);
  
  // LED gets brighter the harder you press
  analogWrite(LEDpin, LEDbrightness); // here you are using PWM !!!
 
  delay(10);
}

```