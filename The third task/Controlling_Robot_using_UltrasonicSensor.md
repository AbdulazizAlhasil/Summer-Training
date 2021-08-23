
# The-Third-Task
المهمه الثالثه للتدريب الصيفي في شركة الأساليب الذكية  
مسار الإلكترونيات والقوى

Controlling_Robot_using_UltrasonicSensor
# روبوت التقييم
قمنا ببرمجة الاردوينو الاول لمعرفة ماذا كان هناك شحص امام الروبوت يقف لمدة 3ثواني وارسال امر تشغيل للشاشه عبر البلوتوث  ولعدم وجود البلوتوث استبدلناه باردوينو اخر يستقبل امر التشغيل ويشغل ليد عوضا عن مقطع فيديو ويحرك الذراع 
 
**1.  Code For First Arduino :**

```ruby

// C++ code
//
const int echoPin = 3;
const int trigPin = 4;


long duration;
int distance; 

void setup() {
  pinMode(trigPin, OUTPUT); // Sets the trigPin as an OUTPUT
  pinMode(12, OUTPUT);
  pinMode(echoPin, INPUT);       // Sets the echoPin as an INPUT
  Serial.begin(9600);            // Serial Communication is starting with 9600 of baudrate speed

}
void loop() {

  while(getDistance() > 25){ }

  int startTime = millis(); 
  
  while(getDistance() <25){ 
   int newTime = millis();        //record the current time

  if (newTime - startTime > 300){ 
   Serial.write("1");            // send message to screen to open
    Serial.println('\n');
    break;                        // get out so only send message once
   
  }
  }
  
  while(getDistance() <25){ }
 
}

int getDistance(){                // defining the function to calculate the distance
   
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
 
  duration = pulseIn(echoPin, HIGH);
  distance = duration * 0.034 / 2;         // Calculating the distance
  
  return distance;
}

 
```
**1.  Code For Scound Arduino :**
```ruby

#include <Servo.h>
Servo servo1;

void setup()
{
Serial.begin(9600);
  pinMode(12, OUTPUT);
   servo1.attach(8);
}

void loop()
{
  if(Serial.available() > 0){
  if(Serial.read() == '1')
    digitalWrite(12, HIGH);
    servo1.write(90);    
    delay(3000);
    digitalWrite(12, LOW);
  }
  
}


```

**3. The circuit  :**

**Move the motor forward**
![Circuit](https://github.com/AbdulazizAlhasil/Summer-Training/blob/main/The%20third%20task/Controlling_RobotArm_using_UltrasonicSensor.png?raw=true)



**3 .The Simulation design  :**

[Click here to show the project in TinkerCad](https://www.tinkercad.com/things/2aFVlHpOv1s-shiny-vihelmo/editel?tenant=circuits)


**ملاحظة  :**
**يرجى فتح الجزء الثاني من المهمه**

