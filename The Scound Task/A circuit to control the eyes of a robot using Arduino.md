
# The-First-Task
المهمه الثانية للتدريب الصيفي في شركة الأساليب الذكية  
مسار الإلكترونيات والقوى

An arduino-circuit to control the robot eyes. It uses PWM to reduce the energy losses in the LEDs.
We connected the LEDs in parallel so if one got open, the other eye is not affected.
 
 
**1.  the code  :**

```ruby

// C++ code
//
void setup()
{
  pinMode(5, OUTPUT);
   pinMode(6, OUTPUT);
}

void loop()
{
  analogWrite(5,35);
  analogWrite(6,35);
 
}

  
 
```

**2. The circuit  :**


![Circuit](https://github.com/AbdulazizAlhasil/Summer-Training/blob/main/The%20Scound%20Task/Terrific%20Wluff.png?raw=true)


**3 .The Simulation design  :**

[Click here to show the project in TinkerCad](https://www.tinkercad.com/things/9omONw1zFqZ-terrific-wluff/editel?tenant=circuits)


**ملاحظة  :**
**يرجى فتح الجزء الثاني من المهمه**
