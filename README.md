# Color-Tracking-Example

https://www.youtube.com/watch?v=D82RCrmWWV8

ENME351: Electronics II Final Project
Nina Horne

**When I am demonstrating with the green marker the processing had crashed which is why the screen is stuck and not instead displaying "can't tell if this is you!"**

The OpenMV Camera extracts the first face's keypoints and matches all other faces it detects with that first face. If it is likely the same face,  a range which I set as "size" greater than 70, then it runs the color tracking example, which tracks an object that is green-ish. This object's x value is converted to servo control (demonstrated on the lego car) and to processing display as a green circle moving left and right. The green LED is lit and processing displays "Same face detected!" If a face does not match the first one, it does not run the color tracking, therefore only allowing the first person control.
This project is inspired by my Gemstone Honors Program project, AIMAR (Artificially Intelligent Medical Assistant Robot), which aims to use AI to aid in healthcare. I have this camera in my possession as a part of my work on AIMAR. In this context, this 351 project could be used for the robot to know which person it is talking to and only authorize certain activities if it sees that person, turn off if it does not detect a face, and control a motor (or other form of actuation) based on what it sees, which could be used to have the robot follow a face or use an object to control something remotely.

My code: https://drive.google.com/file/d/1aQPe...

OpenMV Cam: 
Single color code tracking example: https://github.com/openmv/openmv/blob...

Face tracking example:
https://github.com/openmv/openmv/blob...

two digital pins output: same face (green!), different face (red!)
analog pin outputs x value of green object

Arduino Uno
converts camera values to LED lights, processing, and servo motor

Processing 3
displays "same face detected" or "can't tell if this is the same face"

Sunfounder Servo 55g motor: http://wiki.sunfounder.cc/index.php?t...
rotates -90 to 90 degrees, based on the x value of the moving green object
