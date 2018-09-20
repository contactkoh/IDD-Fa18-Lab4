# Paper Puppets

*A lab report by John Q. Student*

## In this Report

To submit your lab, clone [this repository](https://github.com/FAR-Lab/IDD-Fa18-Lab4). You'll need to describe your design, include a video of your paper display in operation, and upload any code you wrote to make it move.

## Part A. Actuating DC motors

 ![alt text](https://github.com/contactkoh/IDD-Fa18-Lab4/blob/master/DCmotor.jpg)
 
 Video:   [DC motor working](https://youtu.be/5opCuWPJ3xo)
**Link to a video of your virbation motor**

## Part B. Actuating Servo motors
 Video:   [DC motor working](https://youtu.be/5opCuWPJ3xo)

### Part 1. Connect the Servo to your breadboard

 ![alt text](https://github.com/contactkoh/IDD-Fa18-Lab4/blob/master/DCmotor.jpg)

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



## Part D. Paper puppet

**a. Make a video of your proto puppet.**

## Part E. Make it your own

**a. Make a video of your final design.**
 
