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

'![commutator 1](https://www.youtube.com/watch?v=SINxiaI2JwI)'

![commutator1](https://photos.google.com/u/2/photo/AF1QipNJ0Yb_H7lh9VERVTSOturvBo9PbzvuEKo2369r)

* The next step was to add the wire. We wrapped about 10m of copper wire around the cork between the gaps of the copper ring on the commutator. We made sure as we were wrapping the wire around the commutator to count how many turns, In the end we finished with 139 turns. We then soldered the ends of the wires to each side of the copper commutator to complete the circuit. The wire we used was enamelled so that when it was wrapped around the commutator it didnt conduct across, this would slow down the speed of rotation of the armature.

* We then measured the resistance of the coil and got a resistance of about 7.4 ohms.

* After screwing in the paper clips either end of the wood board to act as brackets we set the armature inbetween making sure the nails were supported by the paper clip, but still able to rotate relatively freely. Next we screwed in 2 paperclips on the opposite sides of the coil so that we could place magnets on them to create a magnetic field across the coil. We set the magnets to attract as this is how a motor works by inturupting the magnetic feild between the 2 magnets. We made sure to test the magnets either way to make sure that we did have the correct orientation. 

* For the brushes we decided to start of my just touching the wires to the copper plates but found that this wasnt very effective. We decided to stick the wires each to a piece of copper tape, this gave us a better surface contact with the copper on the armature. 

* We then decided to test how well the motor worked. When supplying the motor with a voltage of about 5v and 2A current limmit we managed to get a decent spin out of it. After some more testing we found that the higher the voltage we supplied the faster it rotated.
We did this by marking the cork and slowly increaseing the voltage, while videoing the motor so that we could see how many spins it did in a given time.  (add speed here)

Lab 2: Building a better motor
------------------------------

* First we started to redesign the commutator on solid works so that we could put 2 coils around it and so the surface for the brushes is smoother. 
There are 2 advantages of having 2 (or more) coils on the armature... 
1. It means that the motor doesnt need a push start it should start rotaing no matter what orientation the motor begins in as there is allways gonna be a force acting on it.
2. It also means that the motor will spin faster as the force acting on i is doubled and it will have slightly more torque.

* To improve the appearance and function of the motor we decided to buy some bearing so that the armature would spin more freely as here wouldnt be as much friction. We also designed brackets for both the magnets and the bearings.

* We then decided to improve the way the brushes worked by soldering the wires to copper table then sticking it to the base and taping it down so that each part was being pushed against the armature. after some testing we found that this isnt the best of soloutions as it was faulty at times.

* If we were to improve the design we would add more turns to each coil as this would increase the current around the commutator therefor incraseing the force crate by the magnetic feild and the coil interacting, this would increase the speed at which the motor is able to rotate and icrease the torque slightly. We would also try and improve the brushes so that they wernt as temperamental. Also i would use an iron core instead of 3D printing it on the armature, this would make the motor turn faster and increase the torque as it would increase the magnetic field strength.

* When printing the stl files the first time i decided to print them on my own printer, however I had a few problems as the print seemed to fail at 70% each time giving unfinised prints. After reading up on it I believe that the printer go damaged during transport to university and the sd card reader became faulty or the sd card was faulty. I decided to get the parts printed at the university but upon reciveing them I relised I gave a bit to much leeway to the sockets for the magnets and bearing, but we decided to use hot glue to keep them in place.

(add stl file or pictures)

Practical 3: Incremental encoder:
=================================

* After some more testing with the motor we decided to change it a bit further by making the gap between the copper plates smaller so that the brushes are always in contact. Also the motor seemed to spin slow, we found out that this was because the second coil wasnt conducting so we resoldered the wire on and the motor seemed to work much better.

* To make the roteing disk we drew a circle on a piece of card and cut it out. Then we cut a triangle out so that the IR led would be seen by the IR reciever. This allows us to measure the time it takes to rotate the disk once and we can use this to work out the speed of the motor. We glued this onto the end of the motor shaft.

* We connected up the components as shown on the circuit diagram on a breadboard to test it worked. but it wasnt working. We tried to test each part by doing a Continuity test, however there was no cross circuiting and each component seemed to connect across. We decided to get it checked however we were told that it should be working. After testing each component seperately we found that the IR led wasnt working. We got a new led and it began to work.

* Next we soldered it all onto a prototype board and tested again and it all worked. We then decided to attatch it to the bearing stand at the end of the motor with hot glue so that it was in the correct position.  

* To test that it worked we connected the encoder to the arduino board and launched the sample code. This seemed to wrok fine, everytime we rotated the motor by hand and the led was visable through the gap the led on the arduino board would light up. This acted as a visual reprentation that the motor had rotated once.

* When we connected the incremental encoder to the motor we had a few problems, one of which was when we provided power to the motor the encoder seemed to detect movement even when it was pointing away from the encoder disk. We believe that this is due to noise from the electronics after testing on an ocillascope we could see that there was indead alot of noise causing it to incorectly read values. We tried connecting all the grounds together but this did not help. Next we tried adding a decoupling capacitor accross the motor terminals however this didnt seem to work. After a discusion with the teachers and we couldnt figure it out we were told to move on and come back to it if we had time the end.

Practical 4: motor control with Arduino
=======================================



Practical 5: stepper motor and arduino
======================================
* As the motor is uni-polar we have 2 extra wires for ground and power, however we want it bi-polar so that it has more torque. so we connected the (blue and red) and the (green and black) and ignored the white and yellow wires. 


Practical 6: robot arm project 
==============================
Servo control
-------------
* we had a problem when trying to use the potentiometer to move the servos we believe that this is because the potentiometer resistance is too low which is why its suddenly jumping positions instead of moving gradually. (add more)


Robot arm project design
------------------------
* We started to look at basic robot arm design on the internet (for example thingiverse). Firstly we took measurements of the servo itself so that we knew how to connect it to the arm. After knowing what the basic structure should be we began work designing the arm in Fusion 360. 

* The first step was to make a simpe bracket to hold the servo in place and screw it into. After doing this we copyed the file several times so that we had a bracket for each part. The base was the first thing to be designed I drew a circle around the bracket giving a bit of leeway. Next I drew another circle 5mm apart giving it a frairly strong base.then I raised it to a height to cover the servo.

* Next was the top of the base, this was designed seperately so that the base was free to rotate. For this I created the circle as in the base and raised it so that the servo would just fit throught the top. I then added the bracket at 90 degrees so that the first arm would be able to fit and rotate. The bracket has a hole to allow the arm to rotate with support on both sides. then inside of the bracket has a whole in the shape of the servo arm so that when the servo arm is inserted it is flush with the top of the base and has something to push on.

* After createing the base I created the first arm this was just a bracket attached to arms to connect to another bracket.these turned by having the arm indented into the side making it flush with the side. The next part of the arm is the same as this one.

* The second arm part is the connection to the claw. its simmilar to the first arm part, however the bracket is replaced by a rotated bracket and wholes for the claw arms. The claw arms are rods with arms coming out with cogs merged with the top. Then this was mirrored to create the second one. These arms are held on by washers. I finished them all of my fileting the edges and indenting roco22 into the sides to make it look better.

* The cogs didnt seem to fit very well together as I didnt have support for them at the top meaning they just moved apart when turned. If I had more time I would try and make these better.

* Once printed I had to do some sanding and drill some holes for the wires as I forgot to add these into the design. Another problem was I forgot to add room on the base for the first arm to rotate so I had to round of the corners alot so it could rotate. Upon testing the servos did struggle to lift the arm however with more time we might be able to power them seperately so that they have enough power to lift the arm. We tested by connecting either one or two servos and found they were much weaker with both connected , I believe that this is because there isnt enough current to power many.



Practical 7: robot arm project ROS
--------------------------
* We had a few problems with finding the ros libary in arduino however we found that this was because we had the web version of arduino installed, so we had to install arduino again through the terminal. We then launched the example code onto the arduino board so we could control the servos. After launcing roscore and rviz we were able to import the urdf example file into rviz and control the servos on the basic design.

* Next we decided to split the tasks so that I did the urdf file and my partner did the arduino part. The first step was to understand the urdf file, I did this by researching the file format then alot of ttrial and error to see what each part was. Then I created a new folder on my computer with the stl files of each part of the arm. 

* I added one stl file at a time to test if it worked, I then used the example code to see the structure and added each joint. After adding each joint and stl files all I had to do was change each parts origin and rotational origin so that it created a representation of the arm in real life.  (add picture of arm)



