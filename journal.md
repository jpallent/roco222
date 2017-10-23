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

Lab 2: Building a DC motor
==========================
Lab 1
-----
* First step is to put the copper tape around the cork leaving 2 gaps so that wire can be wrappped around it.then pushing 2 pins in either side of the cork to act as the shaft for it to spin. We then wraped some tape around the bottom.

* After doing this we wrapped about 10m of copper wire around the cork and commutator. As we wrapped it around we counted how many turns and in the end we finished with 139 turns.we then soldered the ends of the wires to each side of the copper commutator.

* When measureing the resistance of the coil we got a resistance of about 7.4 ohms

* we set the magnets to attract as this is how a motor work it inturupts the magnetic feild betwwen the 2 magnets. 

* when supplying the motor with a voltage and 2A current limmit we managed to get a decent spin out of it. The higher the voltage we supplied the faster it span.

Lab 2:
------

* First we started to redesign the commutator on solid works so that we could put 2 coils around it and so the surface for the brushes is smoother. 

* we then designed some magnet mounts and bearing mounts to support the commutator.
https://guides.github.com/features/mastering-markdown/
*after we designed these we tried to redesign the way the brushes worked so that it was more constant.

P3: Incremental encoder:
------------------------

* We have printed the stl files having a few problems with the printer i was using , however the peices came out functional. we rebuild the motor and soldered everything up.

* The motor seems to be running slower than before , I believe this is due to the fact that we opted to print the motor shaft with the commutator. This means the magnetic feild is not as strong. Also we put less coils on each one. we plan to adjust this in the future labs if we have time.

* We have just soldered the IR light source and detector up and checked that it was working. we then opted to hot glue this on to the bearing stand as this is where the shaft extends out and where we put the encoder disk. 





