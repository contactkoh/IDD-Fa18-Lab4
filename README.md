# Paper Puppets

*A lab report by Hongyun(Kevin) Oh*
ho247@cornell.edu


## In this Report

THIS IS THE BEST AND MOST ENJOYABLE LAB SO FAR! :) 


## Part A. Actuating DC motors
 
**Link to a video of your virbation motor**

Video:   [DC motor working](https://youtu.be/3zkNKT3zdvQ)

 ![alt text](https://github.com/contactkoh/IDD-Fa18-Lab4/blob/master/DCmotor.jpg)

## Part B. Actuating Servo motors
 Video:   [Servo Motor](https://youtu.be/nEDxBitw8-o)

### Part 1. Connect the Servo to your breadboard

 ![alt text](https://github.com/contactkoh/IDD-Fa18-Lab4/blob/master/BreadboardServo.jpg)

**a. Which color wires correspond to power, ground and signal?**

Orange strip goes to pin 9, Red to 5V, Brown to GND


### Part 2. Connect the Servo to your Arduino

**a. Which Arduino pin should the signal line of the servo be attached to?**

pin 9 is attached with the servo.

**b. What aspects of the Servo code control angle or speed?**

pin position is initially set to 0

loop has for statements that writes to servo to move between 0 to 180 and from 180 to 0.
myservo.write(pos)

Speed can be controlled by delay duration for servo to  move from 1 pos to the next 2 pos.
delay(15)

The whole code is below:


void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
}


## Part C. Integrating input and output

**Include a photo/movie of your raw circuit in action.**

Video:   [Servo Motor with raw circuit](https://youtu.be/IAmvl3osk8M)

 ![alt text](https://github.com/contactkoh/IDD-Fa18-Lab4/blob/master/ServoCircuit.jpg)


## Part D. Paper puppet

**a. Make a video of your proto puppet.**

Video:   [Puppet Moving](https://youtu.be/IAmvl3osk8M)

 ![alt text](https://github.com/contactkoh/IDD-Fa18-Lab4/blob/master/Puppet1.jpg)



## Part E. Make it your own

**a. Make a video of your final design.**
 
 Video:   [Puppet Moving my way](https://youtu.be/IAmvl3osk8M)
 
 
 
