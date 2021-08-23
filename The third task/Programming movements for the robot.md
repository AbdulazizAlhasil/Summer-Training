
# The-Third-Task
الجزء الثاني من المهمه الثالثه للتدريب الصيفي في شركة الأساليب الذكية  
مسار الإلكترونيات والقوى


# روبوت التقييم
برممجة حركتين للروبوت بحيث يتم التحكم بهم اذا ضغط العميل على امر من شاشة الروبوت يتم التفاعل معه مثلا :حضنه 
**1.  Code For First Arduino :**

```ruby

// C++ code
//
#include <Servo.h>
Servo s1;  //الكوع الأيمن
Servo s2; //الكتف الأيمن
Servo s3; //قاعدة الذراع الأيمن
Servo s4; //الكوع الأيسر
Servo s5; //الكتف الأيسر
Servo s6; //قاعدة الذراع الأيسر


void setup()
{
  pinMode(13,INPUT);
  pinMode(6,INPUT);
  
  s1.attach(2);
  s2.attach(1);
  s3.attach(0);
  s4.attach(10);
  s5.attach(11);
  s6.attach(12);
}
    

void loop ()
{ 
  if (digitalRead(13)==1)
   // first move, when switch 1 is on 
   // The robot will rise the hand up
  {  s1.write(135);
     s2.write(45);
     s3.write(150);
     s4.write(45);
     s5.write(135);
     s6.write(150);
  }
   else if (digitalRead(6)==1)
    // Second move, when switch 2 is on 
   // The robot will advance hand in from of the screen 
   {  s1.write(93);
      s2.write(93);
      s3.write(93);
      s4.write(93);
      s5.write(93);
      s6.write(93);
   
   }
  
  else 
    /* This puts the arm in the initial position, with the arm
    pointing downward
    When both switch 1,2 are off*/
  {  s1.write(93);
     s2.write(93);
     s3.write(0);
     s4.write(93);
     s5.write(93);
     s6.write(0);
  
  
  }

     


}
 
```


**2. The circuit  :**

**Move the motor forward**
![Circuit](https://github.com/AbdulazizAlhasil/Summer-Training/blob/main/The%20third%20task/Controlling_RobotArm_using_UltrasonicSensor.png?raw=true)



**3 .The Simulation design  :**

[Click here to show the project in TinkerCad](https://www.tinkercad.com/things/klgma9W4OOI-copy-of-robot-arm-servo/editel?tenant=circuits)





