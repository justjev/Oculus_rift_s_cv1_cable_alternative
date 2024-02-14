# Oculus_rift_s_cv1_cable_alternative
This is an attempt at coming up with a affordable diy replacement for the Rift S and CV1 custom cables that are no longer available

#I have done zero editing on this, and it is basically a brain dump of my research from yesterday. Please ignore my egregious grammatical errors and run on sentences.
#
#There was a single reddit comment I am too lazy to find right now that said someone else was trying to document one of the oculus boards on github and meta sued him, this is a message to meta in case that is true: I have no intention of making money from this, I have no intention of releasing any industry secrets, I have no intention of hacking the oculus. This is purely a right to repair issue that is causing good quality vr headsets to become e-waste, which I hope to curb in some way from a purely ethical standpoint. (I am open to working for you guys though if you wanna hire away a hobbyist electrical wizard)

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
I intend to order some male portions of that connector(they cost about 2$) and custom fabricate a breakout pcb to get the wiring correct, afterwards, I will design a pcb that should just plug in, and either use a more common 44pin port(dsub, IDE, etc) that will be mounted on the outside of the headset, or if possible a usb port and a displayport. I will release all the design files here.

Links: 

Best teardown explanation: (use translate) https://forum.gamer.com.tw/C.php?bsn=60606&snA=2818

Someone starting to document the cable pinout: https://www.youtube.com/watch?v=T5_sqlemvmI  (at 4:20 you can see his notes which give enough that I should be able to get the usb wired up following his pinout)

Rift S mips chip: https://www.analogix.com/en/system/files/AA-004747-PB-1-ANX7533_0.pdf

What I beleive is the 44pn connector on the mobo (waiting on mine to come in to measure) https://www.digikey.com/en/products/detail/molex/0559094472/3196929

Part to order that mates with that connector https://www.digikey.com/en/products/detail/molex/0513384473/3197116

Displayport test bed pcb https://www.aliexpress.us/item/1005006099055034.html

USB-C test bed pcb https://a.co/d/awRJzoF

Schematic released by meta of the DK2 (which also uses the same architecure and can be used as a decent reference) https://github.com/facebookarchive/RiftDK2/blob/master/Headset/Electrical/Mainboard/Release/DK2_REV3.3_SCH.pdf

Image of the DK2 mobo https://roadtovrlive-5ea0.kxcdn.com/wp-content/uploads/2017/10/rift-dk2-mainboard.png

Ifixit teardown of CV1 (step 10 has detailed mobo pics) https://www.ifixit.com/Teardown/Oculus+Rift+CV1+Teardown/60612

Decent photos of rift s Mobo (pic 6 and 7) https://imgur.com/gallery/hl4CAqq

What noone has documented is the chip that runs the usb host on the rift s, I am assuming it is under the sheilding that noone has removed for teardowns on the mobo.
So when I get mine ill remove that sheilding and take hi def pics of whats hidin under there. 

-------------------------------------------------------------------
feb 13 24 did video teardown of the busted rift s
opened the ef/heat sheild, pics and videos will be uploaded soon

usb chip is cyusb3304-68ltxc
https://www.infineon.com/cms/en/product/universal-serial-bus/ez-usb-hub-controllers/ez-usb-hx3-usb-5-gbps-hub-controller/cyusb3304-68ltxc/

etrontech eSP7762U Y13 AD023kb09.001
absolutely nothing about that chip on the internet that was useful, found the most similar model number that was on a random page with just random chipnames was esp770
https://www.dzsc.com/E/2570/

searching that lead me to this page where that chip is used as the camera usb chip in the oculus cv!
https://electronics360.globalspec.com/article/6973/teardown-oculus-rift-virtual-reality-cv-hm-a 

that mainly concludes the mysteries of what was hidden, I am curious why this one has no info anywhere, but ill keep digging.

-------------- update, even though i absolutely destroyed the rf shield which damaged the mainboard and the headset was sold as not displaying video, it registered to my account and worked asolutely flawlessly with the official cable, so now its time to make that cable a thing of the past
Possible to just throw a raspi in there and have an open vr OS?

so the test points at the top of the board are interesting, going to try to compare to the dx1 schematics similar ports
