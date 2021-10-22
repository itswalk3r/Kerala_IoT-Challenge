# Kerala IOT Challenge

> Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program “Kerala IoT Challenge 2021”, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.
# About Me
> Hi everyone! I’m ArjunRaj, 4th year Electronics and Communication student from Eranad Knowledge City Technical Campus, Manjeri. I’m here to explore new dimensions in the majestuic world of Internet Of Things, aka IOT. I'm also intrested in similar fields such as Cyber Security, online marketing and creative design.

## Experiment 1 : Hello World LED Blinking

> A basic program similar to printing "*Hello World*" in any programming language. The aim is to blink an LED using **Arduino Uno Board**.

>**Arduino Uno** is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram

![blink](https://user-images.githubusercontent.com/56971600/138449253-04d5a19f-ea6a-44d6-97c3-3450e2bf583b.jpg)

![5h7X9_3102_1627394356](https://user-images.githubusercontent.com/91405741/137279765-8a82a34f-1dc0-4afc-9bd3-a31d7f62c428.png)

## Code

```

int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}

```

## Output

> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/56971600/138453021-bfea8d2b-7785-41f1-ae33-f126c4111825.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 2 : Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.

## Components Required 

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3

## Circuit Diagram

![traffic1](https://user-images.githubusercontent.com/56971600/138451092-736bda3e-40b0-4972-9b18-28af8ae9e0b2.jpg)

![trafic2](https://user-images.githubusercontent.com/56971600/138451124-607ef72f-8888-40b4-ae40-440cbde8367c.jpg)

![yiU1x_3102_1627566759](https://user-images.githubusercontent.com/91405741/137288387-e85f8db9-ae97-49d0-888d-a2fc15e4c496.png)

## Code

```

int redled =10; // initialize digital pin 10.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds
digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}

```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/56971600/138452640-c58e5d56-1abf-4339-95b7-6dce64924fa7.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.

## Components Required

* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

## Circuit Diagram

![chaser](https://user-images.githubusercontent.com/56971600/138451914-a95bf6aa-57fb-44bd-8530-c362d4dd5d5b.jpg)

![s5yR0_3102_1627567167](https://user-images.githubusercontent.com/91405741/137292096-feb60c91-1a9a-474b-a596-300285f7b011.png)

## Code

```

int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(400);        // delay
   }  
}

```

## Output

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/56971600/138452157-1b9f0adc-be08-43e0-8ec9-c8b9ec2ec4ca.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 4 : Button Controlled LED

> An experiment to light an LED using a Push Button.

## Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagrams

![push1](https://user-images.githubusercontent.com/56971600/138453350-97c7cf20-1e3c-48e1-9cf7-dfd24cf78c0e.jpg)

![push2](https://user-images.githubusercontent.com/56971600/138454527-5b05c4fd-0954-41e8-af5a-490ca53a783c.jpg)

![wQGca_3102_1628160139](https://user-images.githubusercontent.com/91405741/137344321-3e662dee-cb00-421d-a34d-848c2ffd1a6f.png)

## Code

```

int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}

```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/56971600/138454296-1d47d56b-7ac2-4c19-8d0a-5953146b94ba.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.

## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

## Circuit Diagrams

![buzzer](https://user-images.githubusercontent.com/56971600/138455178-a20076ac-bc1f-46e7-b86f-96681aced52f.jpg)

![BBr05_3102_1628160460](https://user-images.githubusercontent.com/91405741/137346830-1fa2408c-2a1d-4fdf-a049-5736aeb803ec.png)

![e9Pdc_3102_1628160446](https://user-images.githubusercontent.com/91405741/137346912-0f871dbf-8e86-4734-a337-fceeff454e33.png)

## Code

```

int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}

```

## Output

> The Buzzer makes beep sound.

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/56971600/138455486-b4d8d26b-a52c-43b5-adc4-17a2a396231e.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams

![rgb](https://user-images.githubusercontent.com/56971600/138455771-53b5a7be-11f4-46ae-911e-83c2641f39d6.jpg)

![xX9cw_3102_1628160649](https://user-images.githubusercontent.com/91405741/137347719-6966c0b1-021d-471c-b0a7-48d0441752d0.png)

![A8a40_3102_1628160631](https://user-images.githubusercontent.com/91405741/137347782-e0a8a008-8706-4b7c-ba31-38ef0ab6ca72.png)

![TefdI_3102_1628167200](https://user-images.githubusercontent.com/91405741/137347822-228ccf9c-3a89-45ba-bb24-c3b0ee587818.png)

## Code

```

int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}

```

## Output

> The RGB LED blinks.

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/56971600/138456082-f84e6c10-1f5c-4c4e-8b2b-e0cec9f95cbe.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 7 : LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.

### LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

## Circuit Diagrams

![L5Iw9_3102_1628755894](https://user-images.githubusercontent.com/91405741/138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5.png)

## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

## Circuit Diagrams

![ldr](https://user-images.githubusercontent.com/56971600/138456643-6e97c818-1f8c-4054-bdd5-c25deb9d8775.jpg)

![schema_Myt5vqqplZ](https://user-images.githubusercontent.com/91405741/138436635-60cb2ec4-091d-4f24-bf96-b0289e06fa00.png)

## Procedure

* Connect the 3.3v output of the Arduino to the positive rail of the breadboard
* Connect the ground to the negative rail of the breadboard
* Place the LDR on the breadboard
* Attach the 10K resistor to one of the legs of the LDR
* Connect the A0 pin of the Arduino to the same column where the LDR and resistor is connected (Since the LDR gives out an analog voltage, it is connected to the analog input pin on the Arduino. The Arduino, with its built-in ADC (Analog to Digital Converter), then converts the analog voltage from 0-5V into a digital value in the range of 0-1023). - Now connect the other end of the 10K resistor to the negative rail
* And the the second (free) leg of the LDR to the positive rail
Pretty much this is what we need for the light sensing. Basic circuits like this can be done without an Arduino aswell. However, if you want to log the values and use it to create charts, run other logics etc. I will recomend an Arduino or ESP8266 or may be a ESP32 for this.
Now, as we want our circuit to do something in the real world other than just displaying the values on the computer screen we will be attaching a LED to the circuit. The LED will turn on when its dark and will go off when its bright. To achieve this we will:
* Place the LED on the breadboard
* Connect the 220ohm resistor to the long leg (+ve) of the LED
* Then we will connect the other leg of the resistor to pin number 13 (digital pin) of the Arduino
* and the shorter leg of the LED to the negative rail of the breadboard

## Code

```

const int ledPin = 13;
const int ldrPin = A0;
void setup() {
Serial.begin(9600);
pinMode(ledPin, OUTPUT);
pinMode(ldrPin, INPUT);
}
void loop() {
int ldrStatus = analogRead(ldrPin);
if (ldrStatus <= 200) {
digitalWrite(ledPin, HIGH);
Serial.print("Its DARK, Turn on the LED : ");
Serial.println(ldrStatus);
} else {
digitalWrite(ledPin, LOW);
Serial.print("Its BRIGHT, Turn off the LED : ");
Serial.println(ldrStatus);
}
}

```

## Output

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/56971600/138456973-ff80af12-9fd9-4b8e-b0bb-e819bc13307a.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 8 : Flame Sensor

> We are using Infrared Receiver (IR)for detecting Flame 

## Components Required
* Arduino Uno Board*1
* Flame Sensor *1
* Buzzer *1
* 10K Resistor *1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagram

![image](https://user-images.githubusercontent.com/56971600/138458405-67d985fb-3ea2-4714-87ec-125ccf9ce5c3.png)

## Code

```

int flame=0;// select analog pin 0 for the sensor
int Beep=9;// select digital pin 9 for the buzzer
int val=0;// initialize variable
 void setup() 
{
  pinMode(Beep,OUTPUT);// set LED pin as “output”
 pinMode(flame,INPUT);// set buzzer pin as “input”
 Serial.begin(9600);// set baud rate at “9600”
 } 
void loop() 
{ 
  val=analogRead(flame);// read the analog value of the sensor 
  Serial.println(val);// output and display the analog value
  if(val>=600)// when the analog value is larger than 600, the buzzer will buzz
  {  
   digitalWrite(Beep,HIGH); 
   }else 
   {  
     digitalWrite(Beep,LOW); 
    }
   delay(500); 
}

```

## Output

> The buzzer produces a beep noise when the IR Reciever is exposed to flames.

<iframe width="560" height="315"
src=
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 9 : LM35 Temperature Sensor

> LM35 is a common and easy-to-use temperature sensor.

![image](https://user-images.githubusercontent.com/56971600/138459624-95113dfa-f21f-4677-9c1f-c337a03476af.png)

![image](https://user-images.githubusercontent.com/56971600/138459742-1db27599-5b4e-4bcd-ae48-f809a8371ceb.png)

## Components Required 

> LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing.

> LM35 temperature sensor can produce different voltage by different temperature
When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.
The output temperature is 0℃～100℃, the conversion formula is as follows:

![image](https://user-images.githubusercontent.com/56971600/138460051-cbde66eb-988b-4f15-b350-fb4c29fafa99.png)

## Components Required

* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

## Circuit Diagram 

![image](https://user-images.githubusercontent.com/56971600/138460381-ef0df7aa-f13c-45d8-9131-4b1141053052.png)

![image](https://user-images.githubusercontent.com/56971600/138460454-2eda2604-3b8f-4522-bf98-01e5c31314df.png)

## Code

```

int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}

```

## Output

> Temperature values read by LM35 sensor can be seen in the Serial Moniter.

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/56971600/138461186-49c747f3-2e52-49b8-8a4f-5acf96bc7f7e.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>












 












