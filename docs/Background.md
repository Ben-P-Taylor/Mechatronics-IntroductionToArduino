
# Some Useful Background Information
This is some background information to accompany the discussions

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
