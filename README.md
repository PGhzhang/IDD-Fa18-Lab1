# IDD-Fa18-Lab1: Blink!

**A lab report by Hanyu Zhang**

## Part A. Set Up a Breadboard

[insert a photo of your breadboard setup here]


## Part B. Manually Blink a LED

**a. What color stripes are on a 220 Ohm resistor?**
The color stripes are: red, red, black, black, brown.

**b. What do you have to do to light your LED?**
I have to press the pushbutton to light the LED.



## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**
On the code, I need to change the LED_BUILDIN to 13

**b. What line(s) of code do you need to change to change the rate of blinking?**
dely(1000)
**c. What circuit element would you want to add to protect the board and external LED?**
resistence
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**
delay(15),0.015s
**Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md**
delay(2000)


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[link to your video here; feel free to upload to youtube and just paste in a link here]


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**
yes

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
change the PWM pin to 11 by changing int led = 9 to int led =11

**b. What is analogWrite()? How is that different than digitalWrite()?**
digitalWrite set the pin to either high or low voltage, where high = 5v and low =5
analogWrite() set the PMWpin to a oscilating value which has a pulse length based of the duty cycle specified as the second parameter.

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

**d. Is information stored in your device? Where? How?**

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
