
# The-First-Task
المهمه الثانية للتدريب الصيفي في شركة الأساليب الذكية  
مسار الإلكترونيات والقوى

For DC motor control
 We used h_bridge as its type L293D
 With the ability to control the speed and direction by switch
 
 
**1.  the code  :**

```ruby

// C++ code
//
void setup()
{

  pinMode(13, INPUT);
 pinMode(9, OUTPUT);

  pinMode(10, OUTPUT);
  pinMode(8, OUTPUT);
  pinMode(12, OUTPUT);
   pinMode(6, OUTPUT);
  pinMode(11, OUTPUT);

}

void loop()
{
  int potValue=analogRead(A0); // to read the potentmetr value
  int pwmEn=map(potValue,0,1023,0,255);
   analogWrite(9,pwmEn); // we send the pwm to the en pins
   analogWrite(10,pwmEn);  
   
  

    if (digitalRead(13)==HIGH)  //Move the motor forward
    {  digitalWrite(12,1); 
       digitalWrite(8,1);
       digitalWrite(11,0);
       digitalWrite(6,0); } 
    else //Move the motor backwards
       {  digitalWrite(12,0);
          digitalWrite(8,0);
          digitalWrite(11,1);
          digitalWrite(6,1);  
          }
  
  
  delay(150); // Wait for 150 millisecond(s)
  }
  
  
 
```

**2. The circuit  :**

**Move the motor forward**
![Circuit](https://github.com/AbdulazizAlhasil/Summer-Training/blob/main/The%20Scound%20Task/Dazzling%20Curcan-Fulffy%20(2).png?raw=true)

**Move the motor backwards**
![Circuit](https://github.com/AbdulazizAlhasil/Summer-Training/blob/main/The%20Scound%20Task/Dazzling%20Curcan-Fulffy%20(3).png?raw=true)

**3 .The Simulation design  :**

[Click here to show the project in TinkerCad](https://www.tinkercad.com/things/lVwv6Bv1vDV-dazzling-curcan-fulffy/editel)


**ملاحظة  :**
**يرجى فتح الجزء الثاني من المهمه**
