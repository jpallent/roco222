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

