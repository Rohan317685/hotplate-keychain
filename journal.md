heyo! i'll be journalling here :p 

## Nearly finished schematic (3 hours)
I started getting a general idea of what I need to make it's a hotplate-keychain! 
I'm already almost done with the schematic, I need to move over to footprint's and the PCB ofc. 

It has a mosfet, Xiao MCU, Rotary encoder (PWM controlled so you can set your temperature exactly), thermistor, USB_C powered and a indicator light for safety ⚠️

I learnt a lot about mosfets; their pretty much just big transistors and I also figured out how to route a thermistor I've never used one before lol and I've used a mosfet once before so it's very new to me!
 Overall I didn't run into many problem's but I did have a bit of trouble figuring out how the thermistor worked 
![Image of schematic](https://cdn.hackclub.com/019ed611-0a60-78df-a5b0-49549d8af5e4/2026-06-17-154907_1920x1080_scrot.png) 

So this will just be a very silly keychain hopefully around 90x60mm cause that's plenty to be honest and it will be very portable ofc, I will try to make a cute case for this but no promises since I have a deadline of 1 day for this!

I just realised 5v probably wont be enough for this, I need a usb pd chip and decoupling capacitors which I forgot about bru I will add them after this journal and I've spent 3 hours sofar!

## Finished schematic! (3.1 hours)

I finally finished my schematic I added the deocupling capacitors and a 5v voltage regulator for the sk6812 Mini-E and the Xiao supply!

Also added a Usb pd chip so now this support USB PD upto 20v supply and this should be plenty to work with, finiding the usb pd chip took a awfully long time because I had no clue what I was looking for or what USB PD is to be honest eventually landed on this since it seemed to be the best value for it's money and it's stable. I had a look through it's [Download Datasheet](https://www.laskakit.cz/user/related_files/ch224ds1.pdf) aswell! 

I had to remove some resistors for the USB C port and make some minor adjustments across the schematic aswell here's a picture of my progress sofar:

![Image of schematic](https://cdn.hackclub.com/019ed6a5-b205-7c94-bfce-49a22177f105/2026-06-17-182653_1920x1080_scrot.png) 

Today I learnt I suck at figuring out voltage rails 🥀

## Almost finished PCB (4.2 hours)

This took me a while, I had done some research beforehand but not very deep research. I had to pick the footprint's and the fuse holder case which took around ~30 minutes since I wanted to make it compact but hand solderable. 

I then had multiple serpentine heater iterations, in zig zags and other ways I had to space it out 0.5-1mm and use 0.25 mm routing for a overall trace route of around 4-5 meters which I did; I hit 4.65 meters after around 4 iterations and I tried out the kicad array feature but it sucked so I manually copy pasted.


I also had to use a resistivity formul; it used Length, trace width, copper thickness and after some math's I approximated that it should release 44W of energy which is pretty good for a hotplate that's this small! 

The decoupling capacitors are appropriately placed it took a bit to figure out how close it should be to the components and debugging the DRC error's took way to long I had so many thermal relief error's and I didn't know what they were and I eventually figured out I had to set the pad's to solid in properties and had to fix a lot of clearance issues with the routing itself.

I need to do some PCB art and make the case for this ofc, it's just going to be a simple stand-off case!

here's a couple images: 

![Image of PCB](https://cdn.hackclub.com/019ed859-cb20-71a0-adaa-6f9d9d79064d/2026-06-18-022047_1920x1080_scrot.png) 
![Image of 3d PCB](https://cdn.hackclub.com/019ed85a-4718-71f1-98ca-e09d18f30e80/Pendant.png) 


