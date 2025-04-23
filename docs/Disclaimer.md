# Warning and Disclaimer when using your own Laptop/MacBook

!!! Warning 
    ## Warning and Disclaimer when using your own PC/Mac

    In previous years we have had one or two incidents where student’s laptops have stopped working while connected to course hardware. The exact reason for the damage is unknown, but it is suspected that a voltage spike from the servo affected the power supply/data lines on the USB interface and caused irreparable damage to the connected computer.

    Unfortunately, the SoEEE or MEE cannot accept liability for damage to personal IT systems under these circumstances. If you connect anything to your personal IT equipment, you do so at your own risk and you take responsibility for the consequences. This is especially true if you are working with circuits that you have built. It is recommended that you use the University PCs to do these activities to prevent the potential of damage to your personal equipment.
  
    There are a few discussions on the internet regarding this issue, one of which is:
    
    <debugHL>[https://chipwired.com/can-arduino-damage-your-computer/](https://chipwired.com/can-arduino-damage-your-computer/){target="_blank"}</debugHL>

    It appears that a simple USB Isolator device can mostly overcome these rare occurrences. One such device is the FIT0860 Industrial USB Isolator from DFRobot:
    
    <debugHL>[https://www.dfrobot.com/product-2444.html](https://www.dfrobot.com/product-2444.html){target="_blank"}</debugHL>
    
    This device is available from numerous UK on-line suppliers for approximately £20

    **We will not be providing USB isolators for the Arduino activities on this module.**

    Other USB Isolators range from £15 to more than £200 for an industrialised device. Beware of poor imitations, they may not provide the same protection.
    
    There are further ways of minimizing potential damage to your home computer:

    *  Do not make connections to your circuit while Arduino is connected to the PC.
    *  Check for short circuits or incorrect connections before connecting the Arduino to the PC
    *  Do not power the larger servos, the DC motor or multiple SG90 servos from the power supply lines of the Arduino – you should be using the external power supply, provided.
    *  If using an external source, power the test circuit using the power supply and only connect the ground and signal lines to the Arduino if you are maintaining the connection to the PC.
    *  If you are planning to run your system from a battery pack, and not normally connected to the PC using the USB, then disconnect the wires between the battery and the Arduino before connecting the USB line. 

    These methods are not a definitive answer; but should minimise a potential failure. A USB isolator device is a more robust method to minimise these potential failures.
    
    Just to reiterate, these occurrences are very rare, but there is a potential of problems occurring when connecting any USB device to a computer, especially if it is not a certified device, such as a circuit you have made.

    For more information regarding this issue, please speak to the <span style="font-size: 18px;"> **Lab Academic Lead** </span> during the lab sessions.

    Over the years we have had many hundred students use their personal IT equipment and have only had one or two computer failures that may be due to this issue. Using a USB isolator and following the above points is the best method to protect your personal devices, when connected to an Arduino, but is not 100% guaranteed.

    <p style="text-align: center; font-size: 18px;"> **We recommend using the University computers for these activities.**</p>


    