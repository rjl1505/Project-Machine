Project-Machine
===============

Project 22201
//This is the initial code. Code will eventually be modified for a switch instead of a potentiometer. 

#include <Servo.h>      //Including the servor library in the code
  
 
Servo myservo;          // Sets the servo as myservo
 
int x=0;                
 int potPin = A0;       //Potentiometer is connected to A0 and given an integer
 
void setup () {         //Starting off the code
    myservo.attach(12);  //myservo is set to pin 12
    myservo.write(180);  //and is placed at 180 degree 
 }
  
 void loop ()            //Start loop
 {             
   while (x<1) {
      if(analogRead(potPin) > 150)  //if potpin reads less than 150
      {
        myservo.write (25);         //move servo to position 25 degree
        delay (100);                //then pause for 10th of a second
      }//close if statement
      
     else{                         //if potpin reads greater than 150
        myservo.write (180);        //place servo at 180 degree
        delay(100);                 //pause for 10th of a second
      }//close else statement
      
  }//close while statement
  }//close loop
