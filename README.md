# IDD-Fa18-Lab1: Blink!

**A lab report by Hanyu Zhang**

## Part A. Set Up a Breadboard

![alt text](https://github.com/PGhzhang/IDD-Fa18-Lab1/blob/master/IMG_5890.jpg)


## Part B. Manually Blink a LED

**a. What color stripes are on a 220 Ohm resistor?**

The color stripes are: red, red, black, black, brown.

**b. What do you have to do to light your LED?**

I have to press the pushbutton to close the circut, thus lighting up the LED.



## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

On the code, I need to change every LED_BUILDIN to 13, which is the pin number where LED connected to.

**b. What line(s) of code do you need to change to change the rate of blinking?**

In the loop function, change the parameter in delay() to to manipulate the rate of blinkding. For example, mine is delay(1000).

**c. What circuit element would you want to add to protect the board and external LED?**

Add a resistence to protect the board and external LED.

**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

When I change the code to delay(15), which is 0.015s, I can no longer perceive the LED blinking. To prove to myself that the LED is infact still blinking, I can use Burst Mode on iphone camera to taka a series of photos. If there's any phone in this set caught LED off, it would prove that the LED is still blinking.

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**

[link] https://github.com/PGhzhang/IDD-Fa18-Lab1/blob/master/Blink.ino


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[![](http://img.youtube.com/vi/7ItRcAedLVQ/0.jpg)](http://www.youtube.com/watch?v=7ItRcAedLVQ "")



## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

Yes, the LED to glow the whole turning range of potentiometer。The pot has three terminals. As I twist the knob, it moves the position of the third terminal, adjusting the resistence.



## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

I have to change the PWM pin to 11 by changing int led = 9 to int led =11.

**b. What is analogWrite()? How is that different than digitalWrite()?**

analogWrite() sets the PMWpin an analog value(PMW wave). The pin will generate a wave og specified duty cycle untill next call to analogWrite(). Thus, analogWrite() can be used to adjust the brightness of LED. 
digitalWrite() sets the pin to high or low voltage, where high = 5V and low =0V.

Source: 

https://www.arduino.cc/reference/en/language/functions/analog-io/analogwrite/
https://www.arduino.cc/reference/en/language/functions/digital-io/digitalwrite/

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

I took apart a wireless mouse. It's powered by a 1.5vv battery and the simplied schema is shown in the picture below:
![alt text](https://github.com/PGhzhang/IDD-Fa18-Lab1/blob/master/IMG_5958.JPG)

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

This is a microchip on the board, located next to an optical mouse sensor. I suspect that the microchip converts analog movement of hand into digital signals that can be sent to computer through bluetooth.


**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

There's an optical mouse sensor on device, which measures light relfected back up from the desk, and this value is then sent to computer through microchip. There are also three click buttons on top of the device. When user wants to click and select things on the computer, this action is cuaght by the clicking action sensed by these push buttons.

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

The wireless mouse is powered by a 1.5vv battery. Regulation of power is conducted by multuple resisters scatterd on the circut. 

**d. Is information stored in your device? Where? How?**

I don't think information is stored in anyplace in the mouse. The mouse only transmits siginal to computer. 

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

I decided to put a LED starting from the old LED to ground. Since the circuts around the optical sensor and microchips are complex, I chose to avoid those parts and implant the new LED between the exisitng LED to ground. Thus, current flow from the high voltage to ground. 
![alt text](https://github.com/PGhzhang/IDD-Fa18-Lab1/blob/master/IMG_5959.JPG)

### 3. Build your light!

**Make a video showing off your Frankenlight.**

Schematic is shown in above questions.
[![](http://img.youtube.com/vi/AxaHmBj4HXc/0.jpg)](http://www.youtube.com/watch?v=AxaHmBj4HXc "")


**Include any schematics or photos in your lab write-up.**
