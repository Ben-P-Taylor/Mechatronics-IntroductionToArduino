# Building the Robot Chassis

## Introduction

## Constructing the Robot

The system described in this section is the configuration that the author used during the development of the Introduction to Arduino exercises on this module, as shown in <debugHL>[Fig 1](#chassisPic)</debugHL>. This configuration is the recommended configuration for the exercises during this section of the course.

<figure  markdown="span">
  <a name="chassisPic"></a>
  ![Picture of the completed Robot.](./Images/Robot%201st%20Picture.jpg)
  <figcaption>Picture of the completed robot.</figcaption>
  </figure>

### Adding the mechanical components to the chassis
This section will discuss the assembly of the mechanical system, and [a later section](#ElecConn "Electronic Component Layout and Connections") will discuss the assembly of the electronic circuitry.

<figure  markdown="span">
  <a name="chassislayout"> </a>
  ![Annotated layout of the robot chassis](./Images/LayoutOfRobotChassis.png)
  <figcaption>Annotated layout of the robot chassis.</figcaption>
  </figure>

Due to the design of the robot chassis, some elements of the robot must be constructed in order, due to overlapping parts, see <debugHL>[Fig 2](#chassislayout)</debugHL> for a diagram of the layout. The suggested order of construction is:

1.	Attach the yellow FIT0450 motor to the back of the chassis
1.	Attach the skinny wheel to the motor
1.	Attach the cheap plastic wheels to the front of the chassis
1.	Attach the MG996 servo to the front of the chassis
1.	Attach the IR sensor to Lolly Stick D
1.	Attach the lolly stick to the servo horn
1.	Attach the assembled lolly stick with IR sensor and servo horn to the servo shaft.

#### Attaching the FIT0450 and Skinny wheel

This is the most awkward component to attach to the chassis. 

* Push 2x M3x30 through the motor, from the brass shaft side.
* Carefully insert the motor into the chassis and manipulate it so that the screws are aligned with the screw holes in the chassis side wall.
* With a screwdriver inserted through the access holes in the chassis, push the screws through the holes and use 2x M3 nuts to fasten the motor to the chassis.
* Push the skinny wheel onto the motor shaft and use an M3x6 machine screw to fasten the wheel to the motor shaft.

#### Attaching the Cheap Plastic wheels

!!! Note "Do this Before Attaching The Servo"
    These wheels must be attached before the servo, because the servo obscures access to the screw heads for the left wheel.

The cheap plastic wheels should be attached to the lugs at the front of the chassis M4x20 machine screws. Because these wheels rotate freely, you will either need a pair of <debugHL><a href = "https://www.boltscience.com/pages/twonuts.htm" target="_blank">locking nuts</a></debugHL>, (the method I have used in <debugHL>[Fig 1](#chassisPic)</debugHL>), or using an M4 nylon-insert lock nut – nyloc, to ensure the wheels are secure but free to rotate.


#### Attaching the MG996 Servo

!!! Note "Do this After You Have Attached Both of the Wheels"

The MG996 servo is attached to the robot chassis using 3x M4x12 screws and 1x M4x6 screw, as illustrated in Figure 3. The shorter M4x6 screw is required to ensure that breadboard 2, see <debugHL>[Fig 3](#servoNuts)</debugHL>, will fit into the chassis. If you use an M4x12 screw in this location, the tail of the screw is too long and breadboard 2 will not fit into the space provided in the chassis. Figure 3 illustrates which of the 4 M4 screws should be the M4x6.

<figure  markdown="span">
  <a name="servoNuts"></a>
  ![Fixing screws for the MG996 Servo](./Images/Fixing screws for the MG996 Servo.jpg)
  <figcaption>Fixing screws for the MG996 Servo.</figcaption>
  </figure>

####	Assembling the Lolly Stick D Assembly
The lolly stick assembly comprises of the Sharp IR sensor, a laser cut plywood linkage and a servo horn for the MG996, as shown in <debugHL>[Fig 4](#LollyAss)</debugHL>.

<figure  markdown="span">
  <a name="LollyAss"></a>
  ![Fixing Screws for the Lolly Stick Assembly.](./Images/Fixing Screws for the Lolly Stick Assembly.jpg)
  <figcaption>Fixing Screws for the Lolly Stick Assembly.</figcaption>
  </figure>

It is recommended that you assemble the lolly stick assembly as shown in <debugHL>[Fig 4](#LollyAss)</debugHL>, because this results in the header terminals for the IR sensor being on the top side of the IR sensor, when the lolly stick is in the horizontal position, see <debugHL>[Fig 5](#LollyUp)</debugHL>.

The IR sensor is fixed to the lolly stick with 2x M3x6 screws and 2x M3 nuts, as can be seen in <debugHL>[Fig 4](#LollyAss)</debugHL>.

The servo horn is attached to the lolly stick using 2x M2x8mm Phillips Head Flange Screws. 

!!! Warning "Warning: Sharp Screws"
    The sharp ends of the Flange screws will protrude through the opposite side of the servo horn. Please be careful while handling this assembly to prevent causing minor injury on the protruding screws.

####	Attaching the Lolly Stick D Assembly to the Servo
The servo horn pushed onto the servo MG996 servo shaft, then a M3x6 screw is used to fix it into position. Once attached, ensure the servo can rotate between horizontal and vertical, see Figure 5.

!!! info
    This assembly will require repositioning at the start of the control of the standard servo exercise to ensure that the position is set correctly for the exercise.

<figure  markdown="span">
  <a name="LollyUp"></a>
  ![Pictures of the lolly stick assembly attached to the servo, rotated into the horizontal and vertical positions.](./Images/LollyUp.jpg)
  <figcaption>Pictures of the lolly stick assembly attached to the servo, rotated into the horizontal and vertical positions.</figcaption>
  </figure>

###	Electronic Component Layout and Connections
<a name="ElecConn"></a>

The layout of the electronic components on the breadboard is entirely up to you, but following section illustrates how they were laid out during the design and prototyping stages of these exercises. The author recommends following this layout because it also follows the example code provided for the exercises, and it is a tried and tested layout.

#### Breadboard layouts
  <problemHL>There needs to be a bit more explanation for the connections on the breadboards</problemHL>
  
<debugHL>[Fig 6](#BreadboardComps)</debugHL> show the layout for breadboard 1 and breadboard 2. 

* Breadboard 1 contains the LEDs, button and the motor driver board. 
* Breadboard 2 contains the DC power inlet socket, 10K potentiometer and a 12-way header strip, used to connect the motor power and encoder, MG996 servo and the Sharp IR sensor. 

The location of breadboard 1 and breadboard 2 in the robot chassis is illustrated in <debugHL>[Fig 2](#chassislayout)</debugHL> and shown in the <debugHL>[Fig 1](#chassisPic)</debugHL>.

<figure  markdown="span">
  <a name="BreadboardComps"></a>
  ![Component positioning for breadboard 1 and breadboard 2.](./Images/BreadBoard.jpg)
  <figcaption>Component positioning for (a) breadboard 1 and (b) breadboard 2.</figcaption>
  </figure>

The wiring connections for the components, described in <debugHL>[Fig 6](#BreadboardComps)</debugHL>, will follow after the next section discussing the DC power socket and connection.

<problemHL>There needs to be a bit more explanation for the connections on the breadboards</problemHL>

####	3	External DC Power Socket and Connection
Some of the robot systems draw too much power to be supplied directly from the Arduino, via the USB link. If you were to were to power the MG996 Servo or the DC motor from the Arduino, then you may pull too much power from the +5V rail and experience erratic behaviour due to the Arduino intermittently restarting – this is referred to as a <debugHL><a href = "https://www.allaboutcircuits.com/technical-articles/what-is-brown-out-reset-microcontroller-prevent-false-power-down/" target="_blank">brownout restart</a></debugHL>.
To overcome this problem, we will use an additional external DC power supply to provide extra current capability for some of the components – MG966 servos and DC motor driver board. To facilitate this, you will add a DC power connector to your robot system, shown in <debugHL>[Fig 7](#DcPower)</debugHL>.
 
<figure  markdown="span">
  <a name="DcPower"></a>
  ![Annotated picture of the external power supply connector pins](./Images/BreadBoard.jpg)
  <figcaption>Annotated picture of the external power supply connector pins.</figcaption>
  </figure>
In previous years, we have had problems with the DC power connector slipping out of the breadboard. To significantly reduce the chances of this, a cable tie can be used strap the dc connector down to breadboard 2, as illustrated in <debugHL>[Fig 8](#CableTie)</debugHL>.

<figure  markdown="span">
  <a name="CableTie"></a>
  ![Photograph of the cable tie used to hold the DC power connector and the  positioning of the DC power connector on the breadboard.](./Images/CableTie.jpg)
  <figcaption>Photograph of the cable tie used to hold the DC power connector and the  positioning of the DC power connector on the breadboard.</figcaption>
  </figure>

!!! Note
    Ensure that the cable tie is tight around the board and the connector will not move, before snipping the loose end.

#### Arduino and External Power Supplies Lines

There are two +5V power supplies on the robot chassis:

1. The +5V supply from the Arduino
2. The external +5V from the AC-DC Plug-in Power Supply.

<span style="font-weight:bolder;color:red;">ON NO CIRCUMSTANCE</span> should the +5V lines of these power supplied be connected together. You must, however, connect all the GND lines of these power supplies, and other systems, to a common GND net/node on your robot chassis to ensure that all the working from the same reference voltage.

The external +5V should only be connected to the V<sub>m</sub> connection of the motor drive board and the V+ power connections of any servo used on your system. The Arduino +5V should be used for the V<sub>cc</sub> connection of the motor drive board and any other connection requiring +5V, <span style=color:red;>which is not connected to the external +5V</span>.

!!! Danger "Danger: You can destroy your Laptop motherboard if you get this wrong"
    If you connect the +5V supply of the Arduino and the external power supply together you risk destroying the motherboard of your laptop by sending a voltage spike up the USB lead when the servo or the DC motor operate.

    Read the [Disclaimer](./Disclaimer.md) document before proceeding.

    The University and MEE take no responsibility for damaged laptops due to this issue. We recommend using the University IT equipment to mitigate damaging your personal equipment.

*At this point you may have noticed that we don't want you to connect the external +5V to the Arduino +5V. This is because we don't want to tell any other student that we will not be paying for repairs to their personal IT equipment... <span style=color:red;>It is not a fun conversation to have</span>!*

### Suggested I/O Pin Connections for the Arduino for the Exercises
The electronic system for the robot can be incrementally built as required for the exercise you are working on. The exercises are designed, such that, you only need to add components to the system, with the later exercises build on the previous. This means that no circuitry needs to be removed between exercises.

Before you start any of the following exercises, you will need to add extra elements into your robot circuit.

1. [Basic: LED Pattern](#LEDPatternBuild)
    * No extra circuitry is required for the Calibration of Potentiometer Angle Exercise. This uses the potentiometer from the LED Pattern Exercise.
2. [Basic: IR Sensor Measurement + Graph](#irSensor)
3. [Basic: Externally Powered Servo](#poweredServo)
4. [Basic: DC Motor](#dcMotor)
5. [Basic: Encoders and Motor](#Encoder)

!!! Note "Note: Advanced Exercises" 
    The advanced exercises do not require any extra circuit build. They work from the circuit that has been constructed for the final Basic Exercise: Encoders and Motor.

#### Circuit Layout for the LED Pattern and Calibration of Potentiometer Angle Exercises
<a name="LEDPatternBuild"></a>

The following circuit layout is sufficient to complete both the [LED pattern](./Ex1ledPattern.md) and the [Calibration of Potentiometer Angle](./Ex2PotCalibration.md) Exercises. This section illustrates where to layout and the connections for: the three LEDs and associated resistors, the button and the potentiometer, as illustrated in <debugHL>[Fig. 9](#LEDPattern)</debugHL>.

<figure  markdown="span">
  <a name="LEDPattern"></a>
  ![Diagram showing the suggested component layout and wiring for the LED Pattern Exercise.](./Images/SillyBot LED Pattern.png)
  <figcaption>Diagram showing the suggested component layout and wiring for the LED Pattern Exercise.</figcaption>
  </figure>

The extra components list required for this exercise, shown in <debugHL>[Fig. 9](#LEDPattern)</debugHL>, other than the Arduino and 2x breadboards:

* 3x LED
* 3x 470Ω resistor
* Tactile button
* 100nF capacitor
* Potentiometer
* 12-way header

<debugHL>[Fig. 9](#LEDPattern)</debugHL> illustrates the component layout, but for clarity,<debugHL>[Table 1](#ledPatConnect)</debugHL> lists the connections into the Arduino that we recommend for this section:

<table>
  <a name="ledPatConnect"></a>
  <thead>
    <tr> <th>Arduino Pin:</th> <th>Description:</th> </tr>
  </thead>
  <tbody>
    <tr><td>DIO 4</td><td>Button</td> </tr>    
    <tr><td>DIO 11</td><td>LED 1</td> </tr>    
    <tr><td>DIO 12</td><td>LED 2</td> </tr>    
    <tr><td>DIO 13</td><td>LED 3</td> </tr>    
    <tr><td>A5</td><td>Potentiometer Input</td> </tr>    
  </tbody>
<caption>Suggested Connection table for the LED Pattern Exercise.</caption>
</table>

This circuit layout can be used for the [LED pattern](./Ex1ledPattern.md) and the [Calibration of Potentiometer Angle](./Ex2PotCalibration.md) exercises.

#### Circuit Layout for the IR Sensor Exercise
<a name="irSensor"></a>

This section illustrates the connection of the Sharp IR sensor into the circuit, required for the [IR Sensor Measurement and Graph](./Ex3IrSensor.md) exercise, as illustrated in <debugHL>[Fig. 10](#irSensorPic)</debugHL>. You should keep the circuit wired from the previous section.
 

<figure  markdown="span">
  <a name="irSensorPic"></a>
  ![Diagram showing the suggested component layout and wiring for the IR Sensor Exercise.](./Images/SillyBot IR Sensor.png)
  <figcaption>Diagram showing the suggested component layout and wiring for the IR Sensor Exercise.</figcaption>
  </figure>

 Extra parts required for this configuration:

 * Sharp IR Sensor
 * Sharp IR Sensor cable

 <debugHL>[Table 2](#IRConnect)</debugHL> lists the connections into the Arduino that we recommend for the IR Sensor:

 <table>
  <a name="IRConnect"></a>
  <thead>
    <tr> <th>Arduino Pin:</th> <th>Description:</th> </tr>
  </thead>
  <tbody>
    <tr><td>A4</td><td>IR Sensor Output</td> </tr>    
   
  </tbody>
<caption>Suggested Connection table for the LED Pattern Exercise.</caption>
</table>

The Sharp IR sensor cable has header connections attached to the non-sensor end. The header connections should plug into the 12-way header on the breadboard, in the place illustrated in <debugHL>[Fig. 10](#irSensorPic)</debugHL>.

#### Circuit Layout for the Externally Powered Servo Exercise
<a name="poweredServo"></a>

<figure  markdown="span">
  <a name="powerServoPic"></a>
  ![Diagram showing the suggested component layout and wiring for the Externally Powered Servo Exercise.](./Images/SillyBot Powered Servo.png)
  <figcaption>Diagram showing the suggested component layout and wiring for the Externally Powered Servo Exercise.</figcaption>
  </figure>

  <problemHL>Parts List</problemHL>

#### Circuit Layout for the DC Motor Exercise
<a name="dcMotor"></a>

<figure  markdown="span">
  <a name="dcMotorPic"></a>
  ![Diagram showing the suggested component layout and wiring for the DC Motor Exercise.](./Images/SillyBot dc Motor.png)
  <figcaption>Diagram showing the suggested component layout and wiring for the DC Motor Exercise.</figcaption>
  </figure>

#### Circuit Layout for the Encoders and Motor Exercise
<a name="Encoder"></a>

<figure  markdown="span">
  <a name="EncoderPic"></a>
  ![Diagram showing the suggested component layout and wiring for the Encoders and Motor Exercise.](./Images/SillyBot Encoder.png)
  <figcaption>Diagram showing the suggested component layout and wiring for the Encoders and Motor Exercise.</figcaption>
  </figure>

- aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaah!
- -
- -
- -
- -
- -

<problemHL>This is the old wording before going to Exercise by Exercise</problemHL>
#### Suggested I/O Pin Connections for the Arduino for the Exercises

As discussed in the [Introduction section](./index.md), there are 6 basic exercises and 3 advanced exercises. When constructing you robot, you may either struct it on an exercise-by-exercise basis or build the complete circuit before starting. The exercise list below is colour coded to illustrate, in conjunction with <debugHL>[Table 1](#ArduinoConnect)</debugHL> to illustrate at which point different connections need to be made for the different exercises.

1.	<p style="background-color:#ffff00; color: black">Basic: LED Pattern </p>
2.	Basic: Calibration of Potentiometer Angle 
3.	<p style="background-color:#ff0000; color: white">Basic: IR Sensor Measurement + Graph </p>
4.	<p style="background-color:#00ffff; color: black">Basic: Externally Powered Servo</p>
5.	<p style="background-color:#00ff00; color: black">Basic: DC Motor</p>
6.	<p style="background-color:#ff00ff; color: white">Basic: Encoders + Motor</p>
7.	Advanced: PI Control – Encoder Position
8.	Advanced: PI Control – IR Sensor Distance
9.	Advances: PI Control – IR with Sequence

<debugHL>[Table 1](#ArduinoConnect)</debugHL> shows the connections from the Arduino to the components on the breadboard and those mounted directly to the chassis. Some of the connections listed in <debugHL>[Table 1](#ArduinoConnect)</debugHL> are connected through the header pins, these are indicated in column 3 if connected.

<table>
  <a name="ArduinoConnect"></a>
  <thead>
    <tr> <th>Exercise:</th> <th>Arduino Pin:</th> <th>Header Strip Pin:</th> <th>Description:</th> </tr>
  </thead>
  <tbody>
    <tr> <td>Do Not Connect</td><td>DIO 0</td><td></td><td>N/C – Serial Port Cons for USB UART</td> </tr>    
    <tr> <td>Do Not Connect</td><td>DIO 1</td><td></td><td>N/C – Serial Port Cons for USB UART</td> </tr>    
    <tr class=magenta-row> <td>Exercise 6</td><td>DIO 2</td><td>3</td><td>Encoder B</td> </tr>    
    <tr class=magenta-row> <td>Exercise 6</td><td>DIO 3</td><td>4</td><td>Encoder A</td> </tr>    
    <tr class=yellow-row> <td>Exercise 1</td><td>DIO 4</td><td></td><td>Button</td> </tr>    
    <tr class=green-row> <td>Exercise 5</td><td>DIO 5</td><td></td><td>PWM for Motor Driver</td> </tr>    
    <tr class=cyan-row> <td>Exercise 4</td><td>DIO 6</td><td>7</td><td>PWM for the Servo</td> </tr>    
    <tr class=green-row> <td>Exercise 5</td><td>DIO 7</td><td></td><td>BI1 for Motor Driver</td> </tr>    
    <tr class=green-row> <td>Exercise 5</td><td>DIO 8</td><td></td><td>BI2 for Motor Driver</td> </tr>    
    <tr> <td>None, (Useful for debugging)</td><td>DIO 9</td><td></td><td>Debug Timing</td> </tr>    
    <tr> <td>Not Used</td><td>DIO 10</td><td></td><td>N/C - Spare</td>  </tr>    
    <tr class=yellow-row> <td>Exercise 1</td><td>DIO 11</td><td></td><td>LED 1</td> </tr>    
    <tr class=yellow-row> <td>Exercise 1</td><td>DIO 12</td><td></td><td>LED 2</td> </tr>    
    <tr class=yellow-row> <td>Exercise 1</td><td>DIO 13</td><td></td><td>LED 3</td> </tr>    
    <tr> <td>Not Used</td><td>A0</td><td></td><td>N/C - Spare</td> </tr>    
    <tr> <td>Not Used</td><td>A1</td><td></td><td>N/C - Spare</td> </tr>    
    <tr> <td>Not Used</td><td>A2</td><td></td><td>N/C - Spare</td> </tr>    
    <tr> <td>Not Used</td><td>A3</td><td></td><td>N/C - Spare</td> </tr>    
    <tr class=red-row> <td>Exercise 3</td><td>A4</td><td>12</td><td>IR Sensor Input</td> 
    <tr class=yellow-row> <td>Exercise 1</td><td>A5</td><td></td><td>Potentiometer Input</td> </tr>    
  </tbody>
<caption>Suggested Connection table for the Exercises, highlighting at which stage the connections need to be made.</caption>
</table>

####	The 12-Way Header Connections
The 12-way header connector provides a convenient method for interfacing some of the system components: motor, encoder, servo and, IR sensor, to the breadboard for easy connection to the remaining electrical system. A summary of the connections used in development are provided in <debugHL>[Table 2](#headerConnect)</debugHL>.

<table>
  <a name="headerConnect"></a>
  <thead>
    <tr> <th>Pin:</th><th>Description:</th><th>Connected to:</th> </tr>
  </thead>
  <tbody>
    <tr class=green-row> <td>1</td><td>Motor +</td><td>Driver Board BO1</td> </tr>    
    <tr class=green-row> <td>1</td><td>Motor -</td><td>Driver Board BO2</td> </tr>    
    <tr class=magenta-row> <td>3</td><td>Encoder A Signal</td><td>Arduino DIO 3</td> </tr>    
    <tr class=magenta-row> <td>4</td><td>Encoder B Signal</td><td>Arduino DIO 2</td> </tr>  
    <tr class=magenta-row> <td>5</td><td>Encoder GND</td><td>GND</td> </tr>    
    <tr class=magenta-row> <td>6</td><td>Encoder +5V</td><td>Arduino +5V</td> </tr>    
    <tr class=cyan-row> <td>7</td><td>Servo Signal</td><td>Arduino DIO 6</td> </tr>    
    <tr class=cyan-row> <td>8</td><td>Servo +5V</td><td>External +5V</td> </tr> 
    <tr class=cyan-row> <td>9</td><td>Servo GND</td><td>GND</td> </tr>    
    <tr class=red-row> <td>10</td><td>IR Sensor +5V</td><td>Arduino +5V</td> </tr>    
    <tr class=red-row> <td>11</td><td>IR Sensor GND</td><td>GND</td> </tr>    
    <tr class=red-row> <td >12</td><td>IR Sensor Signal</td><td>Arduino Analogue Input A4</td> </tr>    
  </tbody>
<caption>12-Way Header Connections to robot components.</caption>
</table>

#### TB6612FG Motor Driver Board Connections
Due to the most convenient orientation of the TB6612FG motor driver board on the robot, we will be using channel B for these exercises. The TB6612FG driver board is shown in <debugHL>[Fig 9](#TB6612FG)</debugHL>.

<figure  markdown="span">
  <a name="TB6612FG"></a>
  ![Picture of the TB6612FG motor driver board, with pins labelled.](./Images/TB6612FG.jpg)
  <figcaption>Picture of the TB6612FG motor driver board, with pins labelled.</figcaption>
  </figure>

The connections for the driver board used in the development of the exercises are shown in <debugHL>[Table 3](#TB6612FGConnect)</debugHL>. 

!!! Note
    All the GND connections are internally connected on the breakout board, therefore, only one GND connection is needed to the power system.

<table>
  <a name="TB6612FGConnect"></a>
  <thead>
    <tr> <th>Pin:</th><th>Description:</th><th>Connected to:</th> </tr>
  </thead>
  <tbody>
    <tr> <td>Vm</td><td>Motor Power System Supply</td><td>External +5V</td> </tr>    
    <tr> <td>Vcc</td><td>Logic Control Power Supply</td><td>Arduino +5V</td> </tr>    
    <tr> <td>GND</td><td>Ground</td><td>N/C</td> </tr>    
    <tr> <td>AO1</td><td>Channel A Motor Output 1</td><td>N/C</td> </tr>    
    <tr> <td>AO2</td><td>Channel A Motor Output 2</td><td>N/C</td> </tr>    
    <tr> <td>BO2</td><td>Channel B Motor Output 2</td><td>Motor -</td> </tr>    
    <tr> <td>BO1</td><td>Channel B Motor Output 1</td><td>Motor +</td> </tr>    
    <tr> <td>GND</td><td>Ground</td><td></td> </tr>    
    <tr> <td>PWMA</td><td>Channel A PWM Signal</td><td>N/C</td> </tr>    
    <tr> <td>AI2</td><td>Channel A Bridge Configuration Input 2</td><td>N/C</td> </tr>    
    <tr> <td>AI1</td><td>Channel A Bridge Configuration Input 1</td><td>N/C</td> </tr>    
    <tr> <td>Standby</td><td>Driver Chip Standby Signal</td><td>Arduino +5V</td> </tr>    
    <tr> <td>BI1</td><td>Channel B Bridge Configuration Input 1</td><td>Arduino DIO 8</td> </tr>    
    <tr> <td>BI2</td><td>Channel B Bridge Configuration Input 2</td><td>Arduino DIO 7</td> </tr>    
    <tr> <td>PWMB</td><td>Channel B PWM Signal</td><td>Arduino DIO 5</td> </tr>    
    <tr> <td>GND</td><td>Ground</td><td>Power Supply GND</td> </tr>  
  </tbody>
<caption>Pin connections to the TB6612FG motor driver board.</caption>
</table>

