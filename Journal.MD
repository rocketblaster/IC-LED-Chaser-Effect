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

 Ran into a problem with wiring the diagram in general because I can't end my wire if I don't have a component. I found out that I needed to place the LED and then wire around it.

 ![image](attachments/image6.png)

I think I want to leave pin 5 connected to a 0.01u capacitor to ground. So I made it that way. I picked a 330 resistor for the LEDs at the end since I plan on a 5v supply. I added a connector so I can provide a power source to the PCB.

 ![image](attachments/image7.png)

 The schematic is now organized I think I can move onto the PCB. I built it by following various tutorials and implemented a potentiometer because I want to change the output of the timer between what seems to be pins 2 and 1.

 ![image](attachments/image8.png)

 When I tested out the Design Rules Checker, I ran into a problem where my "input power pin not driven by any output power pin" I tried to do that via a connector but that didn't work.

  ![image](attachments/image9.png)

  So I fixed it by adding power flags and it made the Design Rules Checker happy!

 ![image](attachments/image10.png)

I am sure that this is my final. I picked a low resistor at the end of the LED chain so some current can flow through resulting in average brightness and a 50k potentiometer to adjust.

 ![image](attachments/image11.png)

 Anyhow I updated my PCB from schematic. I can't wait to come up with a PCB outline though within the constraint of 100x100m. This is also a time to start planning a layout with all of my leds hehe. That's after assigning my footprints, I followed another guide which used slightly different footprint for the resistor size, but I researched and people on some forums told me its okay but a little risky due to the size of the holes. It should work though in my personal opinion so I stuck with it.
 
 ![image](attachments/image12.png)

 ### Time Spent: 2 Hours

 ## April 2nd, 2026 - Final Iterations & PCB editing

 I am thinking of changing my JST connector to a battery coin instead, if there is enough space on the PCB, which there shoud be obviously. For sometime I sketched out a dog PCB with the idea of the LEDs aroudn the dog. I feel like it is not that great so I am going to change the outline to a flower because it's like a circular LED chaser circuit.

Earlier on, the circuit I picked is mostly based on the astable circuit data sheet for the 555 timer. I wanted to pick a battery terminal, but in the library I noticed battery and battery cell. I searched it up but also found it in the description. I will probably go with a battery cell as it is a single cell.

I searched up what the battery cell would look like but it would take a lot of space so I reverted back to the pin connectors.

![image](attachments/image13.png)

Anyhow going back to square one to where I was on the pcb editor, I am going to trace an outline of a cherry blossom flower. Obviously I'd need to convert from mm to pixels for what editor software I am using to trace the outline into SVG for the moment.

I created a flower shaped outline for my LED chaser. This time I added a 100x100m box to make sure it fits within the constraint! I hope I can fit my components on there!

![image](attachments/image14.png)

### Time Spent: 1 Hour

## April 3rd, 2026 - PCB layout and Fabrication

Imported to the SVG, tried aligning but no point as long as it is within the constraint of the square. Time to start laying out.

![image](attachments/image15.png)

Added Edge Cuts outline and started to iterate on the most optimal layput

![image](attachments/image16.png)

Started to arrange the layout, goal is to have LEDs on the petals. Unforunately as I follow the blue lines they're pretty far so I'll have to rearrange the IC pins to be close to the LEDs.

![image](attachments/image17.png)

I changed the orientation of LEDs on one side so the traces don't overlap, might use the bottom layer though. I also changed the diodes order to whichever is closest.

![image](attachments/image18.png)

I'm going to test out the traces for this layout now after following my schematic and placing important signal components together

![image](attachments/image19.png)

My layout might need some not work but I think it is so annoying trying to route all of these connections going from one resistor to 10 different leds. I think I will do what is a called a filled zone so everything is one big trace.

![image](attachments/image20.png)

Things are not looking good for the LEDs on the right side, have to deal with unnecessarily long traces. I think I'll do ground pour with some ground traces and rebuild it as there is no space on the top. I ended up with traces from D9 and D8 going to U2. However I think it is the most optimal so far I can get to.

![image](attachments/image21.png)

This one wouldn't go in. I am going to rotate my pontentiometer for this reason I design it this way. I ended up rotating my resistor though and it sorts of works. Due to the lack of space, I am moving some net wires to the bottom layer and using the rebuilding each time I add a new trace.

![image](attachments/image22.png)

After some Design Rules Checker test, I ran into a few problems but they were minor and mostly overlapping traces over solder masks, so I readjusted as needed. I think this is my PCB and I'm hopefully done with it.

![image](attachments/image23.png)

### Time Spent: 1.5 Hours