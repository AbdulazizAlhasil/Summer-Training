
# The-First-Task
المهمه الأولى للتدريب الصيفي في شركة الأساليب الذكية  
مسار الإلكترونيات والقوى

**1.  the code  :**

```ruby

#include <Servo.h>

int pos = 0;

Servo servo_1;
Servo servo_2;
Servo servo_3;
Servo servo_4;
Servo servo_5;

void setup()
{
  servo_1.attach(9);
 servo_2.attach(10);
   servo_3.attach(11);
   servo_4.attach(12);
     servo_5.attach(13);
}

void loop()
{
  // sweep the servo from 0 to 90 degrees in steps
  // of 1 degrees
  for (pos = 0; pos <= 90; ++pos) {
    // tell servo to go to position in variable 'pos'
    servo_1.write(pos);
    servo_2.write(pos);
    servo_3.write(pos);
    servo_4.write(pos);
    servo_5.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
  delay(150);
  for (pos = 90; pos >= 0; --pos ) {
    // tell servo to go to position in variable 'pos'
    servo_1.write(pos);
    servo_2.write(pos);
    servo_3.write(pos);
    servo_4.write(pos);
    servo_5.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
}
```

**2. The circuit  :**


![Circuit](https://github.com/AbdulazizAlhasil/Summer-Training/blob/main/The%20First%20Task/Images/task1%20(1).png?raw=true)



**3 .The Simulation design  :**

[Click here to show the project in TinkerCad](https://www.tinkercad.com/things/54N1QAz5Qb5-glorious-trug)


**ملاحظة  :**
**يرجى فتح الجزء الثاني من المهمه**
