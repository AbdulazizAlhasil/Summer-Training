

# Control of 5 servo motors by means of a variable resistance (potentiometer)

**1.  the code  :**

```ruby

#include <Servo.h>
Servo servo_1;
Servo servo_2;
Servo servo_3;
Servo servo_4;
Servo servo_5;

int AN_1;   
int AN_2,AN_3,AN_4,AN_5; // variable to read the value from the analog 


void setup() {
  
servo_1.attach(9);
servo_2.attach(10);// attaches the servo on pin 11 to the servo object
servo_3.attach(11);
servo_4.attach(12);
servo_5.attach(13);

}

void loop() {
   AN_1 = analogRead(A1);            // reads the value of the potentiometer (value between 0 and 1023)
  AN_1 = map(AN_1, 0, 1023, 0, 180);     // scale it to use it with the servo (value between 0 and 90)
  servo_1.write(AN_1);                  // sets the servo position according to the scaled value
                       


   AN_2 = analogRead(A2);            // reads the value of the potentiometer (value between 0 and 1023)
  AN_2 = map(AN_2, 0, 1023, 0, 180);     // scale it to use it with the servo (value between 0 and 90)
 servo_2.write(AN_2);   // sets the servo position according to the scaled value
 
          AN_3 = analogRead(A3);            // reads the value of the potentiometer (value between 0 and 1023)
  AN_3 = map(AN_3, 0, 1023, 0, 180);     // scale it to use it with the servo (value between 0 and 90)
  servo_3.write(AN_3);     
  
     AN_4 = analogRead(A4);            // reads the value of the potentiometer (value between 0 and 1023)
  AN_4 = map(AN_4, 0, 1023, 0, 180);     // scale it to use it with the servo (value between 0 and 90)
  servo_4.write(AN_4);   
    
     AN_5 = analogRead(A5);            // reads the value of the potentiometer (value between 0 and 1023)
  AN_5 = map(AN_5, 0, 1023, 0, 180);     // scale it to use it with the servo (value between 0 and 90)
  servo_5.write(AN_5);    
  
  delay(15);                           // waits for the servo to get there

  
}
```

**2. The circuit  :**


![Circuit](https://github.com/AbdulazizAlhasil/Summer-Training/blob/main/The%20First%20Task/Images/task1.2.png?raw=true)



**3 .The Simulation design  :**

[Click here to show the project in TinkerCad](https://www.tinkercad.com/things/iWOT75L3wDC-magnificent-jofo)
