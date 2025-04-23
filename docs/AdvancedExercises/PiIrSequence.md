# Sequenced Control of the Robot Chassis

!!! Info "GTA Marking"
    This is an assessed Exercise. When you have completed the <debugHL>[Assessed Exercise](#calibPotEx)</debugHL>, you should show your work to a GTA to get marked.

!!! Note "Before Continuing"
    Before starting these exercises, you should ensure that you have completed all the <debugHL>[Basic Exercises](../BasicExercises/README.md)</debugHL> and have fully constructed the robot chassis, as described in the <debugHL>[Building the Robot](../RobotBuild.md)</debugHL> document.
    
## Introduction

During this exercise, you will integrate all the concepts you have used so far, for both the Basic and Advanced exercises, into one sequence of operations, as described below.


The following video is a quick demonstration of the final outcome from this exercise:

<figure>
<div style="text-align: center;">
<iframe id="kaltura_player" src='https://cdnapisec.kaltura.com/p/2103181/embedPlaykitJs/uiconf_id/53345422?iframeembed=true&amp;entry_id=1_sf98riu0&amp;config%5Bprovider%5D=%7B%22widgetId%22%3A%221_zed54ef2%22%7D&amp;config%5Bplayback%5D=%7B%22startTime%22%3A0%7D'  style="width: 400px;height: 285px;border: 0;" allowfullscreen webkitallowfullscreen mozAllowFullScreen allow="autoplay *; fullscreen *; encrypted-media *" sandbox="allow-downloads allow-forms allow-same-origin allow-scripts allow-top-navigation allow-pointer-lock allow-popups allow-modals allow-orientation-lock allow-popups-to-escape-sandbox allow-presentation allow-top-navigation-by-user-activation" title="IR Sensor Video"></iframe>
</div>
<figcaption>Video demonstrating the expected outcome from this exercise</figcaption>
</figure>

## Assessed Exercise

The sequence of action we expect you to demonstrate is:

* Starting with your robot places approximately 30cm from a target, (a kit box standing on its edge will suffice).
* When the button is pressed, wait for 1 second.
* Lower the lolly stick assembly to the horizontal position.
* Wait 1 second.
* Flash your LEDs 3 times, (on 500ms, off 500ms).
* Raise the lolly stick assembly to the vertical position.
* Wait 1 second.
* Move the robot forwards 15cm, using closed loop PI control and encoder feedback.
* Wait 1 second.
* Move the robot backwards 30cm, using closed loop PI control and encoder feedback.
* Wait 1 second.
* Move the robot forwards 30cm, using closed loop PI control and encoder feedback.
* Wait 1 second.
* Move the robot backwards 15cm, using closed loop PI control and encoder feedback.
* Wait 1 second.
* For the next 20 seconds, track the position of the target to 30cm separation, using closed loop PI control and IR sensor feedback.
* Flash your LEDs 3 times, (on 500ms, off 500ms).
* Stop and wait for a button press.
* When the button is pressed, wait for 1 second - repeat the sequence.

### What do we expect to see from the demonstration?

Show code.

Use above sequence.





!!! Success "Now Get Your Work Marked by a GTA"
    Once you have completed your code and are satisfied with its operation, you should show your work to a GTA for marking.






