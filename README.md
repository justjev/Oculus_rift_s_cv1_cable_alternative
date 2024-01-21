# Oculus_rift_s_cv1_cable_alternative
This is an attempt at coming up with a affordable diy replacement for the Rift S and CV1 custom cables that are no longer available

This started as I saw you can purchase a rift s headset without a cable very cheaply on ebay
After researching why, it turns out the cables are prone to failing, and they are no longer produced due to some issues with the connector sourcing.
People have repaired some of them, but I have found zero documentation on anyone trying to solve the root problem, which lies in the connector.
There are also no fully documented teardowns of the rift s, but the same problem plauges the CV1, which uses a different custom connector, and there are detailed teardowns of that
Researching lead me to determine that in reality they use very similar architecure, the main difference being displayport (s), and hdmi (cv1)
I was able to get enough pictures of Rift S motherboards to determine it should simply support displayport being attached directly to the mips chip.
I also was able to determine that the connector from the custom occulink cable goes directly to a 44 pin b2b molex connector.
So I propose the solution is to use the molex connector instead of the occulink connector.
I ordered a headset without the cable from ebay and will attempt that solution

the cv1 does not have a connector between the occulink one and the mobo, it is soldered directly to the mobo. That will require removing the orignal connector, and soldering directly to the points on the mobo

I will start with taking hi def photos of all parts of the rift s motherboard, and then document the pinout for the 44pin molex connector
I intend to order some male portions of that connector(they cost about 2$) and custom fabricate a breakout pcb to get the wiring correct, afterwards, I will design a pcb that should just plug in, and either use a 44pin dsub port that will be mounted on the outside of the headset, or if possible a usb port and a displayport. I will release all the design files here.
