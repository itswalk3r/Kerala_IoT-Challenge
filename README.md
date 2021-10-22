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
https://user-images.githubusercontent.com/56971600/138449649-0c019ed1-c518-4bf2-b7a8-e7ebdf7af85e.mp4
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>


