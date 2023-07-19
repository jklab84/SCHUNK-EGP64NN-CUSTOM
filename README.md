This is a Guide in order to make a custom end effector and use it with Schunk EGP 64 N N Gripper

There are some things to do:
1) Make a cable in order to connect the "power box" with the gripper.
2) Make a "Powerbox" in order to power the device and send the signals.
3) Connect the "Powerbox" to a computer with a USB cable
4) Write a c script for Arduino (or clone) and upload it (It is in "Powerbox")
5) Make the preparations in order to communicate PC and Arduino (or Clone).
6) Write a Python script in order to send commands to the Gripper .(open/close)

##########################################################################
 1) Make a cable in order to connect the "power box" with the gripper.

For this we will need the "Schunk EGP 64 N N Gripper Manual" -> EGP Operating Manual
https://d16vz4puxlsxm1.cloudfront.net/asset/076200133045-Prod/document_fvi9gggs492glb1dcrnnsi8f1q/EGP%20Operating%20Manual.pdf
At the chapter "5.2.2 Electrical connection - Digital I/O variant" there is the M8 pinout.

The M8 plug colors are:
1) BROWN : 24V DC (+) cable      (right up)
2) WHITE : Open Gripper Command  (right down)
3) BLUE  : GND DC (-) cable      (left up)
4) BLACK : Close Gripper Command (left down)

BE CAREFUL !!!! : This pinout is the pinout of the plug ... we have to invert left/right to power it corectly!!!

The M8 cable colors are:
1) BROWN : 24V DC (+) cable      (left up)
2) WHITE : Open Gripper Command  (left down)
3) BLUE  : GND DC (-) cable      (right up)
4) BLACK : Close Gripper Command (right down)

Now for the other side of the cable I use a 5 pin CB Microphone Plug.

1) BROWN        :  24V DC (+) cable      (left up)
2) WHITE        :  Open Gripper Command  (left down)
3) BLUE         :
4) BLACK        :
5) YELLOW/GREEN :  A cable to a metal chassis of your construction. 

I prefer to connect Male (cable side) to Female ("Powerbox" site) and with a multimeter check the continuity before soldering the ends. 
