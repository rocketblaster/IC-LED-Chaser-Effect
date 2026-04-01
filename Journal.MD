# Project Name

I'm building an LED chaser circuit using 555 timer and a 4017 to create an LED chaser effect. The outline of the PCB will be the shape of an animal to be continued.

## March 30, 2026 - Ideation & Research

Today I worked on researching what I want to make and what ICs I'm going to pick. it seems that I have decided on 555 being a simple oscillator and 4017 for counters. When I got into KiCad there was NE555P and NE555D. I searched it up and one is surface mount while the other one is through hole. I dont plan on having a lot of layers, so I picked the through hole which is NE555P. I reviewed the astable circuit sequence for the 555 timer and identifying which pinouts go to where.

<img width="422" height="580" alt="image1" src="https://github.com/user-attachments/assets/343c7ae3-075f-420a-867e-87e94339022d" />

Decided to go with 4017 the base 10 variant. More outputs would probably suit a lot of LEDs. I researched the 555 timers and I now know where they are, I have to somehow connect it to the 4017 integrated circuit and also find the pinouts for that one. Since I decided to put 555 in astable mode, that means it oscillates. The 4017 is a counter and increases output everytime until it hits a specifc value and resets. So that's cool.

From a website called https://www.build-electronic-circuits.com/4000-series-integrated-circuits/ic-4017/
I found some information of an example LED circuit. This is very simple.

![image](attachments/LED-chaser-circuit.png)

I will reference this and adjust resistor values as needed to change the rate of the LED oscillation.
### Time Spent: 1 Hours

## March 31, 2026 - More researching...

I do want to as some personal touches to my PCB led chaser and I think I'll make a ring of LEDs around a jelly fish shape! I love jellies and they glow :D It's been a hefty week despite being on well not spring break. I'm on spring break but I still have class as a dual enrollment student.

Honestly to save time and learn I'm going to start using a simple blinky board tutorial from Blueprint event so I hope it helps. I plan on making multiple LEDs light up at a time and it seems I just need to connect them both to the specific output.

For now I want to work on the basics so I tried to set up my 10 output of LEDs.

![image](attachments/image2.png)

I read through the data sheet and researched the pinouts for what they mean, for example pin 8 for 4017 leads to ground. I'm not going to use pin 12 for 4017 because I'm not going beyond the 10 counter. I ran into a problem because I don't know where it can be connected to. I searched it up and google told me to just leave it there and it seems like I don't have a place to connect it besides another 4017.

![image](attachments/image3.png)

I made small adjusts for the astable IC circuit. Another problem I will deal with is the timing, do I want my LED to flash rapidly or slowly? I will find a software or website that calculates the timing for the LEDs so I can adjust my resistors or capacitors as needed. I changed my schematic to be a little more organized, because a lot of the circuits I see is in one big series loop.

![image](attachments/image4.png)

### Time Spent: 0.5 Hours

## April 1, 2026 - Time to get locked into to one idea
 
 I continued to make adjusts to my circuit. I decided to change my reference because i wanted to get a raindrop effect type LEDs. They light up like a music stereo if I can describe like that. With a few adjustments obviously and it is not 1:1. Obviously me searching up keywords like "cool LED rain chaser effect" or something like that didn't work. So I had to not rely on youtube videos despite seeing the results and some were not what I was expecting.

 ![image](attachments/led-chaser-by-ic-4017-ic-555.jpg)

 This is my circuit so far, and despite the data sheet saying to leave pin 5 open in the 555, many of the schamatics I saw gave it a small sized capacitor, so it stores a very tiny amount of energy in there. I also linked all of the LEDs together leading to one resistor. My problem is trying to deciding the timing so and I saw one of the resistors was 50k, that big to control the flow?

 ![image](attachments/image5.png)

 ### Time Spent: 0.5 Hours
