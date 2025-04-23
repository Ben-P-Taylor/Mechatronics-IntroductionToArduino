## The Arduino IDE

This section is aimed at providing you with a brief overview into installing and setting up the Arduino IDE, ready for use with these laboratory activities. <debugHL>There are two introductory exercises, presented, which should get you started with uploading code to the Arduino and </debugHL>

### The Installing and Using the Arduino IDE on a University Managed PC

The Arduino software is available on all Managed University PC. In the Electronics and Control Laboratory, the software should already be installed on the workstation and laptop PCs. In other areas of the Diamond and the wider University campus, you may need to install Arduino using the Software Centre application.

**_Note:_** _As you should be aware, you can’t download and install software on the University Managed PC from the internet._

### Installation and Setup of the Arduino Software on your own

**NOTE:** _The procedures laid out in this section are only for use on your home computer. The PCs you will be using in the University laboratories and computer rooms already have the Arduino software installed, or it must be installed from the Managed Desktop software Centre._

**Also Note:** All the documentation for this module assumes you are using a Windows 10 or 11 on a PC. We do not support other operating system versions.

**Information about installing the Arduino IDE can be found on the Arduino website at:** <debugHL>[https://www.arduino.cc/en/Guide/Windows](https://www.arduino.cc/en/Guide/Windows){target="_blank"}</debugHL>

**Procedure:**

Is This working

1. Navigate to the Arduino IDE download page: <debugHL>[https://www.arduino.cc/en/Main/Software](https://www.arduino.cc/en/Main/Software){target="_blank"}</debugHL> download the appropriate version of the Arduino IDE for your operating system.
2. Launch the Arduino IDE, to check it has been installed correctly
3. Ensure you have the latest version of the hardware drivers for the Arduino board:
    - From within the Arduino IDE, select the Tools Menu and navigate to the Board Manager: **Tools** > **Board:** _\[name is the current board\]_ > Boards Manager…
    - From the Boards Manager menu that appears on the left side of the Arduino IDE, Find the **Arduino AVR Boards** item and ensure the latest version of the driver is installed. You can check if there is a more up-to-date version by clicking on the dropdown box in the **Arduino AVR Boards** section, and seeing if there is a higher version available than the installed version indicated at the top of the section – do not install a lower version.


1. At this point you should connect the Arduino Uno to your system and direct the Arduino IDE to the correct Arduino board type and Port to allow your Arduino device to be programmed.
    - It you do not know how to do this, please look at the Getting Started with Arduino UNO guide on the Arduino website: <debugHL>[https://www.arduino.cc/en/Guide/ArduinoUno](https://www.arduino.cc/en/Guide/ArduinoUno){target="_blank"}</debugHL>

## Laboratory Exercises

### Simple Digital I/O

!!! Note
    The remainder of this section is provided for students with no experience of using Arduino and serves as a tutorial example of how to use the Arduino IDE, in its most simple form.

The Arduino microcontroller is a powerful tool to build a wealth of mechatronics and robotic projects. We are just getting started - so let’s introduce how to work with push buttons and LEDs. These elements are digital inputs and outputs, and are representative of the type of actions we typically want in mechatronics projects: we want that upon a command (e.g., pressing a button), an action to take place that can modify the environment in a sensible way (e.g., a noticeable light on or off).

!!! Note
    **Before starting the laboratory exercises**, you should review the contents of the "Mechatronics KIT Information" folder, located in the Lab Practicals (Sem 1) content area of the Blackboard site for the Mechatronics course.

#### Intro Exercise 1: Blink Example

The aim of this exercise is to demonstrate how to upload and run a simple Arduino program.

The Blink example is a good way to test the installation of your Arduino software, and also to identify if there is a major problem with your Arduino hardware.

**Procedure:**

* Load the Blink example from the Arduino IDE files menu: Files > Examples > 01.Basics > Blink, as shown in <debugHL>[Fig. 1](#blink)</debugHL>:

<figure markdown="span">
  <a name="blink"></a>
![Screen shot of how to find the blink example in the Adruino IDE.](../Images/Blink.png)
  <figcaption>Screen shot of how to find the blink example in the Adruino IDE.</figcaption>
</figure>


!!! Note
    The built-in examples, provided in the Arduino IDE, are a great way of finding out how to do certain operations and use some programming constructs.

* You compile and upload your Arduino program, or Sketch, by pressing the Press Upload button, as highlighted with a red circle in <debugHL>[Fig. 2](#upload)</debugHL>:

<figure markdown="span" markdown="span">
  <a name="upload"></a>
![A screen shot of the Upload button, highlighted with a red circuit, in the Arduino IDE.](../Images/Upload.png)
  <figcaption>A screen shot of the Upload button, highlighted with a red circuit, in the Arduino IDE.</figcaption>
</figure>


After the IDE compiles and uploads your program, the Arduino should start to run your code. For this example, this will be indicated by the LED, “L”, (highlighted in Red in <debugHL>[Fig. 3](#ledL)</debugHL>), which should be slowly flashing. (Note: LED “L” is also connected to pin 13).

<figure markdown="span">
  <a name="ledL"></a>
  ![The Arduino Board, with the LED, “L”, highlighted with a red box.](../Images/LED L.png)
  <figcaption>The Arduino Board, with the LED, “L”, highlighted with a red box.</figcaption>
</figure> 

1. The setup() and loop() functions of the Blink example are shown below. Modify the values in the delay() functions, (highlighted in red) and investigate its effects again. What happens?

_(See the Arduino Language Reference, from the Arduino website, for details of the delay() function:<debugHL>[https://www.arduino.cc/reference/en/language/functions/time/delay/](https://www.arduino.cc/reference/en/language/functions/time/delay/){target="_blank"}</debugHL>_)


You should observe that changing the value in the brackets for the upper delay() function, changes the on-time of the LED, and changing the value of the lower delay function, changes the off-time for the LED.

### Intro Exercise 2: Push Button and LED

The aim of this exercise is to use a digital input, in this case from a push button, to trigger the Arduino to produce a digital output. In this case and LED, as illustrated in the circuit shown in <debugHL>[Fig. 4](#ledButton)</debugHL>.

**Wiring Procedure:**

* Using the Kit of parts provided, connect the circuit as shown in <debugHL>[Fig. 4](#ledButton)</debugHL>.
    - It is not essential to maintain the colour of wires illustrated in the diagram.
    - The digital input from the button is connected to pin 2
    - The digital output to the LED is connected to pin 13, (shared with the LED “L” on the Arduino board)
    - The resistor connected between the button and the GND line is 10K, and the resistor connected between the anode of the LED and pin 13 of the Arduino is 470Ω.

!!! Note
    There is a guide to reading resistor values in the Mechatronics Kit Information section of the Blackboard site.

!!! Note
    The digital Input, on pin 2, is ‘pulled’ down to the 0V supply rail by the a 10K resistor, (a resistor used in this manner is often referred to as a pull-down resistor). In this configuration, when we press the button, the digital input is connected to the +5V supply rail. When the button is released, the 10K resistor ‘pulls’ the digital input back down to 0V. without the 10K resistor, the input would ‘float’, and may produce a spurious input when the button is released.

<figure markdown="span">
  <a name="ledButton"></a>
  ![Diagram illustrating the Circuit configuration for the Push Button and LED Exercise.](../Images/ledButton.png)
  <figcaption>Diagram illustrating the Circuit configuration for the Push Button and LED Exercise.</figcaption>
</figure> 

The code for this exercise can be found by selecting the in-built Button exercise from the Files menu in the Arduino IDE: Files > Examples > 02.Digital > Button

**Procedure:**

- Run Button example Arduino sketch: you should see the LED light up when you press the button, and the LED should go out when you release the button.

!!! Note
    It is often the case that we may wish to view data directly from within an Arduino program. To achieve this we can use the Serial library to stream data from the Arduino, across a COM interface (this can be the same COM port you are using to program the Arduino) to a terminal – we can use the Serial Monitor in the Arduino IDE for convenience.


The modified Button example code, <debugHL>[shown below](#buttCode)</debugHL>, is based on the Button example, but has the following two extra lines:

``` Arduino
// Initialise communications with the serial monitor. Parameter: baud rate
Serial.begin(9600);

...and

// Write the value of the buttonState variable to the serial monitor
Serial.println(buttonState);
```

These extra commands initialise the Serial interface, and write data to the COM port. A description of the Serial commands can be found in the Serial functions section of the Arduino reference guide:

<debugHL>[https://www.arduino.cc/reference/en/language/functions/communication/serial/](https://www.arduino.cc/reference/en/language/functions/communication/serial/){target="_blank"}</debugHL>

<a name="buttCode"></a>
``` Arduino title="Modified Button Example"
// constants won't change. They're used here to set pin numbers:
const int buttonPin = 2;  // the number of the push button pin
const int ledPin = 13;    // the number of the LED pin

// variables will change:
int buttonState = 0;  // variable for reading the push button status

void setup() {
  // Initialise communications with the serial monitor. Parameter: baud rate
  Serial.begin(9600);

  // initialize the LED pin as an output:
  pinMode(ledPin, OUTPUT);
  // initialize the push button pin as an input:
  pinMode(buttonPin, INPUT);
}

void loop() {
  // read the state of the push button value:
  buttonState = digitalRead(buttonPin);

  // Write the value of the buttonState variable to the serial monitor
  Serial.println(buttonState);

  // check if the push button is pressed. If it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    // turn LED on:
    digitalWrite(ledPin, HIGH);
  } else {
    // turn LED off:
    digitalWrite(ledPin, LOW);
  }
}

```

Links to all the Serial function descriptions are listed towards the bottom of the <debugHL>[Serial commands reference page](https://www.arduino.cc/reference/en/language/functions/communication/serial/){target="_blank"}</debugHL>.

To open the Serial Monitor, from the Arduino IDE, click the button in the top right of the IDE, as highlighted in <debugHL>[Fig. 5](#SMbutt)</debugHL>.

<figure markdown="span">
  <a name="SMbutt"></a>
  ![Screen shot of the Serial Monitor button, in the Arduino IDE.](../Images/SM Button.png)
  <figcaption>Screen shot of the Serial Monitor button, in the Arduino IDE.</figcaption>
</figure> 


**Procedure:**

- Modify the Button example sketch, and open the Serial Monitor
- Run the code: You should see a ‘1’ printed on the serial monitor when the button is pressed, and the serial monitor should display ‘0’ when the button is released.
