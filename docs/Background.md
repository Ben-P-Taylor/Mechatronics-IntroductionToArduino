
# Some Useful Background Information
<problemHL>This is some background information to accompany the discussions</problemHL>

## Analogue Sensors
Sensors are used in real world applications to measure physical phenomena and convert these into an electrical characteristic, as illustrated in Figure 9.

<debugHL>**Figure 9. Measuring Physical Phenomena with a Sensor**</debugHL>

Most ‘raw’ sensors do not produce a voltage on their output, but instead the output of the sensor has a modified electrical characteristic, in response to a change in the physical phenomenon being measured. Table 2, illustrates some typical examples of different sensor types used in real world applications, and the type of electrical characteristic the output of each sensor exhibits to a change in the measurement variable. 

<table>
  <a name="sensorTable"></a>
  <thead>
    <tr> <th>Phenomena:</th> <th>Sensor Type:</th> <th>Output:</th>  </tr>
  </thead>
  <tbody>
    <tr> <td>Temperature</td><td>Thermocouple</td><td>Voltage</td> </tr>    
    <tr> <td></td><td>Thermistor</td><td>Resistive</td> </tr>    
    <tr> <td>Light</td><td>Photodiode</td><td>Conductive</td> </tr>    
    <tr> <td>Sound</td><td>Microphone</td><td>Voltage or Capacitive</td> </tr>    
    <tr> <td>Force/Pressure</td><td>Strain Gauge</td><td>Resistive</td> </tr>    
    <tr> <td></td><td>Piezoelectric Transducer</td><td>Capacitive</td> </tr>    
    <tr> <td>Displacement</td><td>Potentiometer</td><td>Resistive</td> </tr>    
    <tr> <td></td><td>LVDT/Resolver</td><td>Analogue Phase/Frequency</td> </tr>    
  
  </tbody>
  <caption>Examples of different sensor types and their output characteristics.</caption>
</table>

It can be seen, from <debugHL>[Table 1](#sensorTable)</debugHL>, that the ‘raw’ output of most of the sensors, listed, do not exhibit a voltage output. For those sensors that have a voltage output, the output voltage is not generally of sufficient magnitude and impedance, to be sampled by the system’s analogue to digital converter. As a result, signal conditioning is required to interface the vast majority sensors to a microcontroller system. 

## PWM Control of Actuators ##

PWM is a way of encoding information into a rectangular pulse train. Generally, the period, (and hence the frequency), of the pulse train is maintained constant, and the width of the rectangular pulses are varied – we will assume this definition for the remainder of these laboratory sessions. 
<debugHL>Figure 13a</debugHL> illustrated the time domain waveform of the PWM signal, where the digital waveform has a rising edge at t=t<sub>0</sub>, and a falling edge at t=t<sub>2</sub>. The on-state of the PWM signal is defined as t<sub>on</sub>, the off-state of the signal is defined as t<sub>off</sub>, and the PWM period is defined as T<sub>s</sub>.

<debugHL>**Figure 13. Pulse Width Modulation, (left) time domain waveforms, (rich) average voltage of PWM signal.**</debugHL>

PWM can be used in a number of different ways; the most common being to ‘chop’ a DC voltage to reduce its average value, as illustrated graphically in Figure 13. The input voltage, V<sub>in</sub> is ‘chopped’, using a converter circuit, into pulses, as shown in Figure 13 (left), where the time integral of the on-state of the waveform is <debugHL>t<sub>on</sub> x V<sub>in</sub>, </debugHL>and has a graphical area of A. The filtering effect of the system we are driving will effectively spread the area under the pulse across in, <debugHL>Figure 13 (left)</debugHL>, across the switching period, Ts, as illustrated in <debugHL>Figure 13 (right)</debugHL>. 

This can be expressed as an integral equation:

<a name="eqn1"></a>
$$
V_{ave} = \frac{1}{T} \int_{t_0}^{t_2} V_{in} dt = \frac{t_{on}} {T_{s}}V_{in}
$$

Where: V<sub>in</sub> is the supply voltage, and V<sub>ave</sub> is the average value of the waveform.

This method of operation is used in most electrical power converters to control the power supply to downstream system, such as a motor.
Another way in which PWM can be used, is to encode some information as a function of the on-state time, t<sub>on</sub>, whilst maintaining a constant switching period, T<sub>s</sub>. The PWM signal is then decoded by the downstream system and a decision is made on its value.

During the laboratory exercises, you will be driving two different types of actuators:

1.	A DC motor - to control the speed of rotation, you will need to control the PWM to regulator the average voltage being fed to the DC motor. To interface the motor to the Arduino, you will need to use a motor drive circuit, to supply the current requirements of the motor.
2.	A standard servomotor - this servomotor will move between 0 and 180 degrees and the angle can be controlled through a 5V pulse signal between 1-2ms and an embedded potentiometer

<problemHL> Add a picture showing the difference between the two types of motor</problemHL>

The DC motor is different from the standard servomotor, in terms of the type of control. For servomotors, the average value of the PWM signal is not being used to regulate the average supply voltage to the device, like it is for DC motors, but instead, the PWM on-time is bounded between 2 values, (1ms and 2ms in this case), and is an encoded signal relating to a rotational position demand parameter for the servomotor, closed loop, controller.