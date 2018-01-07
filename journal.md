What is markdown?
=================

markdown is a way to style text on the web.It allows you to mcontrol the display of the document e.g ( formating word into italic , adding images,creatings lists ...) It is just regular text with some non-alphabetic characters put in.

Key syntax rules
================

Headers 
-------
you can use put the '#' key in front of a sentence to make it a header, and '##' for a sub header and so on...

Emphasis 
--------
you can use either '*' or _ either side of a word or sentence to make it italic 
or 
'**' or '__' to make it bold 

Lists
-----
for lists you can use either '*' for unordered or '1.' and so on for an ordered list 

Images 
------
you can add an image by using '![Alt Text](url)' 

Links 
-----
you can add links by using '[Alt Text](url)' 

Blockquotes 
-----------
you can use '>' at the front of a sentence to nmake it a block quote


# Step 2 the terminal 
----------------------
* ls shows the available folders in the current directory 
* cd /tmp is a tempory directory that is very fast 
* cd $home this takes you back to the home directory 
* mkdir makes a directory 
* echo "Hello"> hello.md echo alone recals the text all of it creates a md file in the directory with the text in it
* cat hello.md displays text withing a file 
* cp hello.md hello-again.md copys tect file and renames new file to new name 
* mv hello-again.md hello-hello.md moves and renames file
* rm hello.md removeds / deletes file
* rm -rf removes file 
* cat / proc/cpuinfo opens and displays content of file


Using git
---------
git uses a localy repository on you pc to md files and git files that can be uploadecd to the git hub repository which is a clone of the one created on the system. 

you can use git add "filename" to add a file to your localy reprosity and git commit to commit it to git hub with a title.

git log shows the history of changes to the git reprosity.

Hacking the robot!
------------------
the first thing we did was find the ip address of the robot, we did this by connecting to the robot on the internet by typing chapman.local and loggging in using nao as username and password.
We then clicked the connection to get the ip address.

one we found the ip address we conected to the robot through the terminal by using ssh nao@192.168.0.184 (which was the ip address) and again the password was nao

after we were loged in we started python by simply typing phython.

now we wrote the sample code provided...
from naoqi import ALProxy
tts = ALProxy("ALTextToSpeech", "localhost", 9559)
tts.say("I've hacked you, robot!")

this allowed us to get the robot to speak :)

Practical 2: Building a DC motor
================================
Lab 1: Building a basic commutator
-----------------------------------

* The first thing we did was putting the copper tape around the cork,making sure to leave 2 gaps so that wire can be wrappped around it.  next we pushed 2 pins in either side of the cork to act as the shaft for it to spin on. to finish it off we added some black table around the middle section to keep the copper in place.

* The next step was to add the wire. We wrapped about 10m of copper wire around the cork between the gaps of the copper ring on the commutator. We made sure as we were wrapping the wire around the commutator to count how many turns, In the end we finished with 139 turns. We then soldered the ends of the wires to each side of the copper commutator to complete the circuit. The wire we used was enamelled so that when it was wrapped around the commutator it didnt conduct across, this would slow down the speed of rotation of the armature.

* We then measured the resistance of the coil and got a resistance of about 7.4 ohms.

* After screwing in the paper clips either end of the wood board to act as brackets we set the armature inbetween making sure the nails were supported by the paper clip, but still able to rotate relatively freely. Next we screwed in 2 paperclips on the opposite sides of the coil so that we could place magnets on them to create a magnetic field across the coil. We set the magnets to attract as this is how a motor works by inturupting the magnetic feild between the 2 magnets. We made sure to test the magnets either way to make sure that we did have the correct orientation. 

* For the brushes we decided to start of my just touching the wires to the copper plates but found that this wasnt very effective. We decided to stick the wires each to a piece of copper tape, this gave us a better surface contact with the copper on the armature. 

* We then decided to test how well the motor worked. When supplying the motor with a voltage of about 5v and 2A current limmit we managed to get a decent spin out of it. After some more testing we found that the higher the voltage we supplied the faster it rotated.
We did this by marking the cork and slowly increaseing the voltage, while videoing the motor so that we could see how many spins it did in a given time.  (add speed here)

Lab 2: Building a better motor
------------------------------

* First we started to redesign the commutator on solid works so that we could put 2 coils around it and so the surface for the brushes is smoother. There are 2 advantages of having 2 (or more) coils on he armature is
1. It means that the motor doesnt need a push start it should start rotaing no matter what orientation the motor begins in as there is allways gonna be a force acting on it.
2. It also means that the motor will spin faster as the force acting on i is doubled and it will have slightly more torque.

* To improve the appearance and function of the motor we decided to buy some bearing so that the armature would spin more freely as here wouldnt be as much friction. We also designed brackets for both the magnets and the bearings.

* We then decided to improve the way the brushes worked by soldering the wires to copper table then sticking it to the base and taping it down so that each part was being pushed against the armature. after some testing we found that this isnt the best of soloutions as it was faulty at times.

* If we were to improve the design we would add more turns to each coil as this would increase the current around the commutator therefor incraseing the force crate by the magnetic feild and the coil interacting, this would increase the speed at which the motor is able to rotate and icrease the torque slightly. We would also try and improve the brushes so that they wernt as temperamental.

* When printing the stl files the first time i decided to print them on my own printer, however I had a few problems as the print seemed to fail at 70% each time giving unfinised prints. After reading up on it I believe that the printer go damaged during transport to university and the sd card reader became faulty or the sd card was faulty. I decided to get the parts printed at the university but upon reciveing them I relised I gave a bit to much leeway to the sockets for the magnets and bearing, but we decided to use hot glue to keep them in place.

(add stl file or pictures)

Practical 3: Incremental encoder:
=================================

* The motor seems to be running slower than before , I believe this is due to the fact that we opted to print the motor shaft with the commutator. This means the magnetic feild is not as strong. Also we put less coils on each one. we plan to adjust this in the future labs if we have time.

* We have just soldered the IR light source and detector up and checked that it was working. we then opted to hot glue this on to the bearing stand as this is where the shaft extends out and where we put the encoder disk. 

We had alot of problems tring to get the circuit to work as one of the components was faulty but after 2 attempts at the circuit it finally works. 

* once connected to the arduino the led blinks when the motor is spun

* when we connected the incremental encoder to the motor we had a few problems, one of which was when we provided power to the motor the encoder seemed to detect movement even when it was pointing away from the encoder disk. We believe that this is due to noise from the electronics after testing on an ocillascope we could see that there was indead alot of noise causing it to read values. we tried connecting all the grounds but this did not help . we then tried adding a decoupling capacitor accross the motor terminals this ...... (add more)

Practical 4: motor control with Arduino
=======================================



Practical 5: stepper motor and arduino
======================================
* As the motor is uni-polar we have 2 extra wires for ground and power, however we want it bi-polar so that it has more tourque. so we connected the (blue and red) and the (green and black) and ignored the white and yellow wires. 


Practical 6: robot arm project 
==============================
Servo control
-------------
* we had a problem when trying to use the potentiometer to move the servos we believe that this is because the potentiometer resistance is too low which is why its suddenly jumping positions instead of moving gradually. (add more)


robot arm project design
-----------------------------
* We started to look at basic robot arm design on the internet for example thingiverse. After knowing what the basic structure should be we began work designing the arm in fusion 360. i finished the design but made a simple error of having one part of the servo mount out of line. after changing that and then setting the point of origin as the turning point i was then able to export as stl to print and use in ros software.


Practical 7: robot arm project ROS
--------------------------
* we had a few problems with finding the ros libary in arduino we found that this was because we had the web version of arduino installed so we had to install arduino again through the terminal. 



