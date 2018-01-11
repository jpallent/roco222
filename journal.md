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
* ls shows the available folders in the current directory * cd /tmp is a tempory directory that is very fast 
* cd $home this takes you back to the home directory 
* mkdir makes a directory 
* echo "Hello"> hello.md echo alone recals the text all of it creates a md file in the directory with the text in it
* cat hello.md displays text withing a file 
* cp hello.md hello-again.md copys tect file and renames new file to new name * mv hello-again.md hello-hello.md moves and renames file
* rm hello.md removeds / deletes file * rm -rf removes file 
* cat / proc/cpuinfo opens and displays content of file

Using git
---------
git uses a localy repository on you pc to md files and git files that can be uploadecd to the git hub repository which is a clone of the one created on the system. 

you can use git add "filename" to add a file to your localy reprosity and git commit to commit it to git hub with a title.

git log shows the history of changes to the git reprosity.

Hacking the robot!
------------------
the first thing we did was find the ip address of the robot, we did this by connecting to the robot on the internet by typing chapman.local and loggging in using nao as username and password. We then clicked the connection to get the ip address.

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

![Step1 Image][Image3]

[Image3]: https://github.com/jpallent/roco222/blob/master/IMG_0219.JPG "basic commutator" 

![Step2 Image][Image4]

[Image4]: https://github.com/jpallent/roco222/blob/master/IMG_0220.JPG "basic commutator"

* The next step was to add the wire. We wrapped about 10m of copper wire around the cork between the gaps of the copper ring on the commutator. We made sure as we were wrapping the wire around the commutator to count how many turns, In the end we finished with 139 turns. We then soldered the ends of the wires to each side of the copper commutator to complete the circuit. The wire we used was enamelled so that when it was wrapped around the commutator it didnt conduct across, this would slow down the speed of rotation of the armature.

![Step3 Image][Image5]

[Image5]: https://github.com/jpallent/roco222/blob/master/IMG_0221.JPG "basic commutator"

* We then measured the resistance of the coil and got a resistance of about 7.4 ohms.

* After screwing in the paper clips either end of the wood board to act as brackets we set the armature inbetween making sure the nails were supported by the paper clip, but still able to rotate relatively freely. Next we screwed in 2 paperclips on the opposite sides of the coil so that we could place magnets on them to create a magnetic field across the coil. We set the magnets to attract as this is how a motor works by inturupting the magnetic feild between the 2 magnets. We made sure to test the magnets either way to make sure that we did have the correct orientation. 

[Opposing Magnets](https://www.youtube.com/watch?v=h_XL3oUzkJ0)

![Step4 Image][Image6]

[Image6]: https://github.com/jpallent/roco222/blob/master/IMG_0222.JPG "basic commutator"

![Step5 Image][Image7]

[Image7]: https://github.com/jpallent/roco222/blob/master/IMG_0223.JPG "basic commutator"

* For the brushes we decided to start of my just touching the wires to the copper plates but found that this wasnt very effective. We decided to stick the wires each to a piece of copper tape, this gave us a better surface contact with the copper on the armature. 

* We then decided to test how well the motor worked. When supplying the motor with a voltage of about 5v and 2A current limmit we managed to get a decent spin out of it. After some more testing we found that the higher the voltage we supplied the faster it rotated.
We did this by marking the cork and slowly increaseing the voltage, while videoing the motor so that we could see how many spins it did in a given time.  (add speed here)

[Wire brushes](https://www.youtube.com/watch?v=h_XL3oUzkJ0)

[Copper tape brushes](https://www.youtube.com/watch?v=ZZyAr5DxDUE)



Lab 2: Building a better motor
------------------------------

* First we started to redesign the commutator on solid works so that we could put 2 coils around it and so the surface for the brushes is smoother. 
There are 2 advantages of having 2 (or more) coils on the armature... 
1. It means that the motor doesnt need a push start it should start rotaing no matter what orientation the motor begins in as there is allways gonna be a force acting on it.
2. It also means that the motor will spin faster as the force acting on i is doubled and it will have slightly more torque.

* To improve the appearance and function of the motor we decided to buy some bearing so that the armature would spin more freely as here wouldnt be as much friction. We also designed brackets for both the magnets and the bearings.

![Step8 Image][Image8]

[Image8]: https://github.com/jpallent/roco222/blob/master/IMG_0235.JPG "basic commutator"

![Step9 Image][Image9]

[Image9]: https://github.com/jpallent/roco222/blob/master/IMG_0236.JPG "basic commutator"
 
[Redesigned motor](https://www.youtube.com/watch?v=wWGUu8mAfnQ&feature=youtu.be)

* We then decided to improve the way the brushes worked by soldering the wires to copper table then sticking it to the base and taping it down so that each part was being pushed against the armature. after some testing we found that this isnt the best of soloutions as it was faulty at times.
* If we were to improve the design we would add more turns to each coil as this would increase the current around the commutator therefor incraseing the force crate by the magnetic feild and the coil interacting, this would increase the speed at which the motor is able to rotate and icrease the torque slightly. We would also try and improve the brushes so that they wernt as temperamental. Also i would use an iron core instead of 3D printing it on the armature, this would make the motor turn faster and increase the torque as it would increase the magnetic field strength.

* When printing the stl files the first time i decided to print them on my own printer, however I had a few problems as the print seemed to fail at 70% each time giving unfinised prints. After reading up on it I believe that the printer go damaged during transport to university and the sd card reader became faulty or the sd card was faulty. I decided to get the parts printed at the university but upon reciveing them I relised I gave a bit to much leeway to the sockets for the magnets and bearing, but we decided to use hot glue to keep them in place.

(add stl file or pictures)

Practical 3: Incremental encoder:
=================================

```cpp
const byte ledPin = 13;
const byte interruptPin = 2;
volatile byte state = LOW;

void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(interruptPin, INPUT);
  // configure the interrupt call-back: blink is called everytime the pin
  // goes from low to high.
  attachInterrupt(digitalPinToInterrupt(interruptPin), blink, RISING);
}

void loop() {
  digitalWrite(ledPin, state);
}

void blink() {
  state = !state;
}
```


* After some more testing with the motor we decided to change it a bit further by making the gap between the copper plates smaller so that the brushes are always in contact. Also the motor seemed to spin slow, we found out that this was because the second coil wasnt conducting so we resoldered the wire on and the motor seemed to work much better.

* To make the roteing disk we drew a circle on a piece of card and cut it out. Then we cut a triangle out so that the IR led would be seen by the IR reciever. This allows us to measure the time it takes to rotate the disk once and we can use this to work out the speed of the motor. We glued this onto the end of the motor shaft.

* We connected up the components as shown on the circuit diagram on a breadboard to test it worked. but it wasnt working. We tried to test each part by doing a Continuity test, however there was no cross circuiting and each component seemed to connect across. We decided to get it checked however we were told that it should be working. After testing each component seperately we found that the IR led wasnt working. We got a new led and it began to work.

* Next we soldered it all onto a prototype board and tested again and it all worked. We then decided to attatch it to the bearing stand at the end of the motor with hot glue so that it was in the correct position.  

* To test that it worked we connected the encoder to the arduino board and launched the sample code. This seemed to wrok fine, everytime we rotated the motor by hand and the led was visable through the gap the led on the arduino board would light up. This acted as a visual reprentation that the motor had rotated once.

* When we connected the incremental encoder to the motor we had a few problems, one of which was when we provided power to the motor the encoder seemed to detect movement even when it was pointing away from the encoder disk. We believe that this is due to noise from the electronics after testing on an ocillascope we could see that there was indead alot of noise causing it to incorectly read values. We tried connecting all the grounds together but this did not help. Next we tried adding a decoupling capacitor accross the motor terminals however this didnt seem to work. After a discusion with the teachers and we couldnt figure it out we were told to move on and come back to it if we had time the end.

[Encoder test](https://www.youtube.com/watch?v=vn7QSk69KVY)

![Step24 Image][Image24]

[Image24]: https://github.com/jpallent/roco222/blob/master/encoder.jpg

![Step10 Image][Image10]

[Image10]: https://github.com/jpallent/roco222/blob/master/IMG_0237.JPG 

![Step15 Image][Image15]

[Image15]: https://github.com/jpallent/roco222/blob/master/IMG_0246.JPG 

![Step16 Image][Image16]

[Image16]: https://github.com/jpallent/roco222/blob/master/IMG_0247.JPG 



Practical 4: motor control with Arduino
=======================================

* Step one is to place the motor shield onto the arduino board as shown: 
![Step25 Image][Image25]

[Image25]: https://github.com/NodrogJRB/ROCO222/blob/master/Images2/Practical_4/I_1_1.jpg?raw=true

This code is used to make the motor rotate :
![Step26 Image][Image26]

[Image26]: https://github.com/jpallent/roco222/blob/master/motor1.jpg

```cpp
void setup() {
  //Setup Channel A
  pinMode(12, OUTPUT);
  pinMode(9, OUTPUT);
}

void loop() {
  //forward @ full speed
  digitalWrite(12, HIGH); //Establishes forward direction of Channel A
  digitalWrite(9, LOW); //Disengage the Brake for Channel A
  analogWrite(3, 255); //Spins the motor on Channel A at full speed
  delay(3000);
  digitalWrite(9, HIGH); //Eengage the Brake for Channel A
  delay(1000);
  
  //backward @ half speed
  digitalWrite(12, LOW); //Establishes backward direction of Channel A
  digitalWrite(9, LOW); //Disengage the Brake for Channel A
  analogWrite(3, 123); //Spins the motor on Channel A at half speed
  delay(3000);
  digitalWrite(9, HIGH); //Eengage the Brake for Channel A
  delay(1000);
}
```

The code tells us that pin 12 controls the direction the motor spins, pin 3 controls the speed at which it rotates and pin 9 is the break. we can set direction and speed by setting their pins as either HIGH or LOW and we can enable the break by setting it HIGH. The max speed the motor can go would be set by setting it to 255 and the min speed by setting it to 0.

Practical 5: stepper motor and arduino
======================================
initial code
-------------
```cpp
#define DIR_A 12
#define PWM_A 3

#define DIR_B 13
#define PWM_B 11

#define MAX 255

unsigned int speed = 5; //Min = 2

//Channel A is 12 & 9 ; Speed is 3
//Channel B is 13 & 8 ; Speed is 11

void turn(){
    analogWrite(PWM_A,MAX);
    analogWrite(PWM_B,0);
    delay(speed);
    
    analogWrite(PWM_A,0);
    analogWrite(PWM_B,MAX);
    delay(speed);
}

void rotate(unsigned int step){
   unsigned int i;
   for(i=0;i<(step);i++){
    digitalWrite(DIR_A,HIGH);
    digitalWrite(DIR_B,HIGH);
    
    turn();
    
    digitalWrite(DIR_A,LOW);
    digitalWrite(DIR_B,LOW);
    
    turn();
   }
}

void setup() {
    //Setup Channel A
    pinMode(DIR_A, OUTPUT);
    
    pinMode(DIR_B, OUTPUT);
}



void loop() {
    //forward at full speed
  rotate(50);
  while(1);
    
}
```

* As the motor is uni-polar we have 2 extra wires for ground and power, however we want it bi-polar so that it has more torque. so we connected the (blue and red) and the (green and black) and ignored the white and yellow wires. 

The Schematics are as followed:

![Schematic Image][Image17]

[Image17]: https://github.com/NodrogJRB/ROCO222/blob/master/Images2/Practical_5/II_1_1.png?raw=true "Wire Schematic"

With wire configuration like this:

![config Image][Image18]

[Image18]: https://github.com/NodrogJRB/ROCO222/blob/master/Images2/Practical_5/II_1_2.jpg?raw=true "Wire configuration" 

![config Image][Image19]

[Image19]: https://github.com/NodrogJRB/ROCO222/blob/master/Images2/Practical_5/II_1_3.jpg?raw=true "Wire configuration" 

Full-step mode:
---------------

```cpp
#define DIR_A 12
#define PWM_A 3

#define DIR_B 13
#define PWM_B 11

#define MAX 255

unsigned int speed = 5; //Min = 2

//Channel A is 12 & 9 ; Speed is 3
//Channel B is 13 & 8 ; Speed is 11

void full_step(){
    digitalWrite(DIR_A,HIGH);
    digitalWrite(DIR_B,HIGH);
    
    analogWrite(PWM_A,MAX);
    analogWrite(PWM_B,0);
    delay(speed);
    
    analogWrite(PWM_A,0);
    analogWrite(PWM_B,MAX);
    delay(speed);

    digitalWrite(DIR_A,LOW);
    digitalWrite(DIR_B,LOW);

    analogWrite(PWM_A,MAX);
    analogWrite(PWM_B,0);
    delay(speed);
    
    analogWrite(PWM_A,0);
    analogWrite(PWM_B,MAX);
    delay(speed);
}

void rotate(unsigned int step){
   unsigned int i;
   for(i=0;i<(step);i++){
      full_step();
   }
}

void setup() {
    //Setup Channel A
    pinMode(DIR_A, OUTPUT);
    
    pinMode(DIR_B, OUTPUT);
}



void loop() {
    //forward at full speed
  rotate(1);
    
}
```

![Step20 Image][Image20]

[Image20]: https://github.com/jpallent/roco222/blob/master/full%20step.jpg "Full step"


Full step mode works by activateing a single phase at a time. However due to only the one phase being in use there is very little torque and it causes the motor to vibrate alot , because there is only 1 force acting on each end at a time.


[Stepper motor 1: Full-step mode](https://www.youtube.com/watch?v=RJmsSzU62jI&feature=youtu.be)

![Step21 Image][Image21]

[Image21]: https://github.com/jpallent/roco222/blob/master/IMG_0238.JPG "stepper motor"

Double-step mode:
-----------------
```cpp
#define DIR_A 12
#define PWM_A 3

#define DIR_B 13
#define PWM_B 11

#define MAX 255

unsigned int speed = 5; //Min = 2

//Channel A is 12 & 9 ; Speed is 3
//Channel B is 13 & 8 ; Speed is 11

void double_step(){
    digitalWrite(DIR_A,HIGH);
    digitalWrite(DIR_B,HIGH);
    
    analogWrite(PWM_A,MAX);
    analogWrite(PWM_B,MAX);
    delay(speed);

    digitalWrite(DIR_A,LOW);
    delay(speed);
    digitalWrite(DIR_B,LOW);
    delay(speed);
    digitalWrite(DIR_A,HIGH);
    delay(speed);
}

void rotate(unsigned int step){
   unsigned int i;
   for(i=0;i<(step);i++){
      double_step();
   }
}

void setup() {
    //Setup Channel A
    pinMode(DIR_A, OUTPUT);
    
    pinMode(DIR_B, OUTPUT);
}



void loop() {
    //forward at full speed
  rotate(1);
    
}
```

![Step22 Image][Image22]

[Image22]: https://github.com/jpallent/roco222/blob/master/double%20step.jpg "Double-step"

Double-step mode work by haveing both phases activated at a time meaning there is always and acctractive force and a replelling force acting at each end meaning that the motor is running with maximum torque. 
[Stepper motor 2: Double-step mode](https://www.youtube.com/watch?v=UdCte2OhZEI&feature=youtu.be)


Half-step mode:
---------------
```cpp
#define DIR_A 12
#define PWM_A 3

#define DIR_B 13
#define PWM_B 11

#define MAX 255

unsigned int speed = 5; //Min = 2

//Channel A is 12 & 9 ; Speed is 3
//Channel B is 13 & 8 ; Speed is 11

void half_step(){
    digitalWrite(DIR_A,HIGH);
    digitalWrite(DIR_B,HIGH);
    
    analogWrite(PWM_A,MAX);
    analogWrite(PWM_B,0);
    delay(speed);
    
    analogWrite(PWM_B,MAX);
    delay(speed);

    analogWrite(PWM_A,0);
    delay(speed);

    digitalWrite(DIR_A,LOW);
    analogWrite(PWM_A,MAX);
    delay(speed);
    
    digitalWrite(DIR_B,LOW);
    analogWrite(PWM_B,0);

    analogWrite(PWM_B,MAX);
    delay(speed);
    
    analogWrite(PWM_A,0);
    delay(speed);

    digitalWrite(DIR_A,HIGH);
    analogWrite(PWM_A,MAX);
}

void rotate(unsigned int step){
   unsigned int i;
   for(i=0;i<(step);i++){
      half_step();
   }
}

void setup() {
    //Setup Channel A
    pinMode(DIR_A, OUTPUT);
    
    pinMode(DIR_B, OUTPUT);
}



void loop() {
    //forward at full speed
  rotate(1);
    
}
```

![Step23 Image][Image23]

[Image23]: https://github.com/jpallent/roco222/blob/master/half%20step.jpg "Half-step"

Half-step mode works by alternating having both phases activated to having a single phase activated. By doing this we have a very similar torque to the previous mode , maybe slighly less but it does increase the angular resoloutin of the motor.
[Stepper motor 3: Half-step mode](https://www.youtube.com/watch?v=TFesuTKz0_M)

Micro-step mode:
----------------
```cpp
#define DIR_A 12
#define PWM_A 3

#define DIR_B 13
#define PWM_B 11

#define MAX 255

unsigned int speed = 5; //Min = 2

//Channel A is 12 & 9 ; Speed is 3
//Channel B is 13 & 8 ; Speed is 11

void WriteValue(int value, int chanAnalog, int chanDigit) //Not able to create -255 voltage, changes to 255, and sets HIGH to LOW
{
  int vaueAbs = abs(value); //Get absolute value
  analogWrite(chanAnalog, value); //Write absolue value as pwm
  if(value > 0){
    digitalWrite(chanDigit,HIGH);
  }
  else{
    digitalWrite(chanDigit,LOW);
  }
}

//Micro_Step//////////////////////////////////////////////////////////
int microsteps = 200; //Howmany steps for one rotation (200)
float amp = 255; //Max output
int pulseDelay = 10; //microseconds between write
int a[200];
int b[200];
int idxG;

void micro_step_INIT(){
  int idx;
  idxG=0;

  for (idx = 0; idx < microsteps; idx++)
  {
    a[idx] = amp * sin(idx * 2  * PI / microsteps); //Builds Sin and Cos tables (2*pi for radians)
    b[idx] = amp * cos(idx * 2 * PI / microsteps);
  }
}

void setup() {
    //Setup Channel A
    Serial.begin(9600);
    
    pinMode(DIR_A, OUTPUT);
    pinMode(PWM_A, OUTPUT);
    
    pinMode(DIR_B, OUTPUT);
    pinMode(PWM_B, OUTPUT);

    digitalWrite(8, LOW);
    digitalWrite(9, LOW);

    micro_step_INIT();
}



void loop() {
    //forward at full speed
  WriteValue(a[idxG], PWM_A, DIR_A);
  WriteValue(b[idxG], PWM_B, DIR_B);
  idxG++;
  
  if(idxG == microsteps){
    idxG = 0;
  }

    delayMicroseconds(pulseDelay);
}
```

Micro-step mode works by incraseing and reducing the power to each part gradually like a ac waveform. By doing this we arnt losing much torque if any but the movements of the motor becomes much smoother because the power is gradually changing it doesnt jump to the next position so quickly, therefor it does not vibrate as much.
[Stepper motor 4: Micro-step mode](https://www.youtube.com/watch?v=uSPSt5KofKA&feature=youtu.be)

Practical 6: robot arm project 
==============================
Servo control
-------------
* We had a problem when trying to use the potentiometer to move the servos we believe that this is because the potentiometer resistance is too low which is why its suddenly jumping positions instead of moving gradually. After some more testing with the servo we managed to get it to run a bit more smoothly. The way it moves is reperesented as a sine wave , this is bacause we want it to gradually slow down when its reaching its limits making it a smoother transition bettween the direction of spin.

Sweep code
----------
```cpp
#include <Servo.h>

#define PWM_A 5

Servo servo_A;

//WAVE GEN
int steps = 200;
float pos = 90;
int pulse = 25;
int sine[200];
int idxG;

void sineGen()
{
  int idx;
  idxG=0;

  for(idx = 0; idx < steps; idx++)
  {
    sine[idx] = (pos * sin(idx * 2 * PI / steps))+90;
  }
}

void setup() {
  // set the digital pin as output:
  servo_A.attach(PWM_A);

  sineGen();
}

void loop() {
  servo_A.write(sine[idxG++]);
  if(idxG == 200){idxG = 0;}
  delay(pulse);
}
```
[Servo control without potentiometer](https://www.youtube.com/watch?v=Ndkt1RIQ37k&t=0s)

Potentiometer code
------------------
```cpp
#include <Servo.h>

#define PWM_A 5

#define dial 0

Servo servo_A;

int value = 0;

void dialControl(){
  value = analogRead(dial);
  
  Serial.print(value);
  Serial.print(" => ");
  value = map(value,0,1023,0,180);
  Serial.print(value);
  Serial.print("\n");

  servo_A.write(value);
  delay(15);
}

void setup() {
  // set the digital pin as output:
  Serial.begin(9600);
  
  servo_A.attach(PWM_A);

  pinMode(dial,INPUT); 

}

void loop() {
  dialControl();
}
```

[Servo control with potentiometer](https://www.youtube.com/watch?v=bU45XKqbKYc&feature=youtu.be)

Now we had to get the arduino code and the servo to move with the arm on the software. To do this we had to write some code to control the nodes.

```cpp
//Include Packages
#include <ros.h>
#include <std_msgs/UInt16.h>
#include <Servo.h>

using namespace ros; //location

NodeHandle nh; //Node declare
Servo servo; //Servo declare

void cb(const std_msgs::UInt16 & msg) //Uses 16 bit (UInt16) message as input, writes the data of
{                                     //the message to the servo.
  servo.write(msg.data); //Write 0 - 180 to servo 
}

Subscriber<std_msgs::UInt16> sub("servo", cb); //Creates sub of "servo" cb

void setup()
{
  nh.initNode(); //Initialise Node
  nh.subscribe(sub);
  
  servo.attach(9); //Attach to pin 9
}

void loop()
{
  nh.spinOnce();
  delay(1);
}
```
before this can do anything we had to launch the ros node through the terminal.
To control the servo we had to publish the angle (0-180) to the rostopic 

```terminal
ben@b-gordon:~$ rostopic pub /servo std_msgs/UInt16 "data: 0"
publishing and latching message. Press ctrl-C to terminate
^C  
ben@b-gordon:~$ 
ben@b-gordon:~$ rostopic pub /servo std_msgs/UInt16 "data: 1800"
publishing and latching message. Press ctrl-C to terminate
```


Robot arm project design
------------------------
* We started to look at basic robot arm design on the internet (for example thingiverse). Firstly we took measurements of the servo itself so that we knew how to connect it to the arm. After knowing what the basic structure should be we began work designing the arm in Fusion 360. 

* The first step was to make a simpe bracket to hold the servo in place and screw it into. After doing this we copyed the file several times so that we had a bracket for each part. The base was the first thing to be designed I drew a circle around the bracket giving a bit of leeway. Next I drew another circle 5mm apart giving it a frairly strong base.then I raised it to a height to cover the servo.[Base 1](https://github.com/jpallent/roco222/blob/master/base%202.stl)


* Next was the top of the base, this was designed seperately so that the base was free to rotate. For this I created the circle as in the base and raised it so that the servo would just fit throught the top. I then added the bracket at 90 degrees so that the first arm would be able to fit and rotate. The bracket has a hole to allow the arm to rotate with support on both sides. then inside of the bracket has a whole in the shape of the servo arm so that when the servo arm is inserted it is flush with the top of the base and has something to push on. .[Base 2](https://github.com/jpallent/roco222/blob/master/base%201.stl)

* After createing the base I created the first arm this was just a bracket attached to arms to connect to another bracket.these turned by having the arm indented into the side making it flush with the side. The next part of the arm is the same as this one. [Arm 2](https://github.com/jpallent/roco222/blob/master/bracket1.stl)

* The second arm part is the connection to the claw. its simmilar to the first arm part, however the bracket is replaced by a rotated bracket and wholes for the claw arms. The claw arms are rods with arms coming out with cogs merged with the top. Then this was mirrored to create the second one. These arms are held on by washers. I finished them all of my fileting the edges and indenting roco22 into the sides to make it look better.
[Arm 3](https://github.com/jpallent/roco222/blob/master/Claw1.stl)

* The cogs didnt seem to fit very well together as I didnt have support for them at the top meaning they just moved apart when turned. If I had more time I would try and make these better. [Claw 1](https://github.com/jpallent/roco222/blob/master/clawarm1.stl), [Claw 2](https://github.com/jpallent/roco222/blob/master/clawarm2.stl), [Cog](https://github.com/jpallent/roco222/blob/master/cog.stl) and [Washer](https://github.com/jpallent/roco222/blob/master/holder.stl)

* Once printed I had to do some sanding and drill some holes for the wires as I forgot to add these into the design. Another problem was I forgot to add room on the base for the first arm to rotate so I had to round of the corners alot so it could rotate. Upon testing the servos did struggle to lift the arm however with more time we might be able to power them seperately so that they have enough power to lift the arm. We tested by connecting either one or two servos and found they were much weaker with both connected , I believe that this is because there isnt enough current to power many.





Practical 7: robot arm project ROS
--------------------------
* We had a few problems with finding the ros libary in arduino however we found that this was because we had the web version of arduino installed, so we had to install arduino again through the terminal. We then launched the example code onto the arduino board so we could control the servos. After launcing roscore and rviz we were able to import the urdf example file into rviz and control the servos on the basic design.

* Next we decided to split the tasks so that I did the urdf file and my partner did the arduino part. The first step was to understand the urdf file, I did this by researching the file format then alot of trial and error to see what each part was. Then I created a new folder on my computer with the stl files of each part of the arm and the urdf file. 

I followed the layout of the example urdf file to gain an understanding of what the file did. this basic code is what was used to get the first basic arm up onto RViz as shown below.

```urdf
<?xml version="1.0"?>
<robot name="roco_arm">
	<link name="base_link">
		<visual>
			<geometry>
				<cylinder length="0.06" radius="0.1"/>
			</geometry>
		</visual>
	</link>
	
	<link name="first_segment">
		<visual>
			<geometry>
				<box size="0.6 0.05 0.1"/>
			</geometry>
			<origin rpy="0 0 0" xyz="-0.3 0 0"/>
		</visual>
	</link>
	
<joint name="base_to_first" type="revolute">
		<axis xyz="0 1 0"/>
		<limit effort="1000" lower="0" upper="3.14" velocity="0.5"/>
		<parent link="base_link"/>
		<child link="first_segment"/>
		<origin xyz="0 0 0.03"/>
	</joint>
</robot>

```
from this we can see that they are all combined into a part called robot, so this must be the main body for the arm. Then we can see that there are 2 different parts inside, the joint and the link. the link is the part you are using for example this is where you insert the stl file. the joint is how you connect the 2 links. The parent link is the one which it having the child link revolve around. Its important to have set the origin on the stl file as the part will revolve around the origin so this can mess up the file if its not in the correct place. The origin in the code is used to tell the part where to be and rpy is used to change the rotation of the object.

* I added one stl file at a time to test if it worked, I then used the example code to see the structure and added each joint. After adding each joint and stl files all I had to do was change each parts origin and rotational origin so that it created a representation of the arm in real life.  

Final arm urdf file
-------------------
```urdf
<?xml version="1.0"?>
<robot name="roco_arm"> <!--name of robot-->
		
	
	<!--<link name="bottom_base"> <!-name of part->
		<visual>
			<geometry>
				<mesh filename = "file:///home/jpallent/Desktop/robot-project/models/parts/base.stl"/> <!-link to model file->
			</geometry>
		</visual>
	</link>
	
	<link name="top_base">
		<visual>
			<geometry>
				<mesh filename = "file:///home/jpallent/Desktop/robot-project/models/parts/base1.stl"/>
			</geometry>
		</visual>
	</link>-->
	
	<link name="first_segment">
		<visual>
			<geometry>
				<mesh filename = "file:///home/jpallent/Desktop/robot-project/models/parts/arm1.stl"/>
			</geometry>
			<!--origin rpy="0 0 0" xyz="-0.3 0 0"/-->
		</visual>
	</link>

	<link name="second_segment">
		<visual>
			<geometry>
				<mesh filename = "file:///home/jpallent/Desktop/robot-project/models/parts/arm1.stl"/>
			</geometry>
			<!--origin rpy="0 0 0" xyz="-0.3 0 0"/-->
		</visual>
	</link>

	<link name="claw_segment">
		<visual>
			<geometry>
				<mesh filename = "file:///home/jpallent/Desktop/robot-project/models/parts/claw1.stl"/>
			</geometry>
			
		</visual>
	</link>

	<!--<link name="first_claw">
		<visual>
			<geometry>
				<mesh filename = "file:///home/jpallent/Desktop/robot-project/models/parts/clawarm2.stl"/>
			</geometry>
			<!-origin rpy="0 0 0" xyz="-0.3 0 0"/->
		</visual>
	</link>

	<link name="second_claw">
		<visual>
			<geometry>
				<mesh filename = "file:///home/jpallent/Desktop/robot-project/models/parts/clawarm1.stl"/>
			</geometry>
			<!-origin rpy="0 0 0" xyz="-0.3 0 0"/->
		</visual>
	</link>-->
	

	<!--<joint name="bottom_base_to_top_base" type="revolute">
		<axis xyz="0 1 0"/>
		<limit effort="1000" lower="0" upper="3.14" velocity="0.5"/>
		<parent link="bottom_base"/>
		<child link="top_base"/>
		<origin xyz="0 25 0" rpy="0 0 3.15"/>
	</joint>

	<joint name="top_base_to_first_segment" type="revolute">
		<axis xyz="0 1 0"/>
		<limit effort="1000" lower="0" upper="3.14" velocity="0.5"/>
		<parent link="top_base"/>
		<child link="first_segment"/>
		<origin xyz="0 -15 0" rpy="1.5 0 0"/>
	</joint>-->

	<joint name="first_segment_to_second_segment" type="revolute">
		<axis xyz="0 1 0"/>
		<limit effort="1000" lower="0" upper="3.14" velocity="0.5"/>
		<parent link="first_segment"/>
		<child link="second_segment"/>
		<origin xyz="-70 0 0" rpy="0 -1.5 0"/>
	</joint>

	<joint name="second_segment_to_claw_segment" type="revolute">
		<axis xyz="0 1 0"/>
		<limit effort="1000" lower="0" upper="3.14" velocity="0.5"/>
		<parent link="second_segment"/>
		<child link="claw_segment"/>
		<origin xyz="-70 0 0" rpy="0 -1.5 0"/>
	</joint>

	<!--<joint name="claw_segment_to_first_claw" type="revolute">
		<axis xyz="0 -1 0"/>
		<limit effort="1000" lower="0" upper="1.57" velocity="0.5"/>
		<parent link="claw_segment"/>
		<child link="first_claw"/>
		<origin xyz="-75 13 -20" rpy="-1.6 3.1 1.57"/>
		<mimic joint="claw_segment_to_second_claw"/>
	</joint>

	<joint name="claw_segment_to_second_claw" type="revolute">
		<axis xyz="0 1 0"/>
		<limit effort="1000" lower="0" upper="1.57" velocity="0.5"/>
		<parent link="claw_segment"/>
		<child link="second_claw"/>
		<origin xyz="-75 -3 -22" rpy="-1.6 3.1 1.57"/>
	</joint>-->
</robot>
```



Opening the joint state gui:
----------------------------
![Step30 Image][Image30]

[Image30]: https://github.com/NodrogJRB/ROCO222/blob/master/Images2/Practical_7/II_1_1.png?raw=true

Setting up RViz:
----------------
![Step31 Image][Image31]

[Image31]: https://github.com/NodrogJRB/ROCO222/blob/master/Images2/Practical_7/II_1_2.png?raw=true

Basic arm in Rviz:
------------------
![Step12 Image][Image12]

[Image12]: https://github.com/NodrogJRB/ROCO222/blob/master/Images2/Practical_7/II_1_3.png?raw=true.JPG 

Finished arm in RViz:
---------------------
![Step13 Image][Image13]

[Image13]: https://github.com/jpallent/roco222/blob/master/IMG_0243.JPG 


Due to the fact that we were using 5 servos we initially tried to control all five servos howver his did not work, one reason this couldnt work was because there was insufficient power to control more than 2 as there wasnt enough current. We could fix this by powering the servos with a external power supply , this will also help give them more torque as they did struggle a bit when lifting the arm. The other reason we could not do this was because there is a limit to the amount of infomation able to transfered by the serial line. we could potentially be able to control more but the amount of infomation being sent for example the name of the joint is taking up alot of the space, if we created an int array to put this infomation in we could save some space and therefor be able to control more nodes. But we havent had any success with this yet.

Robot arm code
---------------
```cpp
//Include Packages
#include <ros.h>
#include <sensor_msgs/JointState.h>
#include <Servo.h>

using namespace ros; //location

NodeHandle nh; //Node declare
Servo base; //Servo declare
Servo link1;
Servo link2;
Servo link3;
Servo claw;

#define BASE  2
#define LINK1 3
#define LINK2 4
#define LINK3 5
#define CLAW  6

void cb(const sensor_msgs::JointState& msg) //Uses 16 bit (UInt16) message as input, writes the data of
{                                     //the message to the servo.
  //int angle_base  = (int)(msg.position[0] * 180/3.14); //conversion from angle in radions to degrees
  //int angle_link1 = (int)(msg.position[1] * 180/3.14);
  int angle_link2 = (int)(msg.position[0] * 180/3.14);
  int angle_link3 = (int)(msg.position[1] * 180/3.14);
  //int angle_claw  = (int)(msg.position[3] * 180/3.14);
  
  //base.write(angle_base); //Write 0 - 180 to servo;
  //link1.write(angle_link1);
  link2.write(angle_link2);
  link3.write(angle_link3);
  //claw.write(angle_claw);
}

Subscriber<sensor_msgs::JointState> sub("joint_states", cb); //Creates sub of "servo" cb

void setup()
{
  nh.initNode(); //Initialise Node
  nh.subscribe(sub);
  
  //base.attach(2); //Attach to pin 9
  //link1.attach(3);
  link2.attach(4);
  link3.attach(5);
  //claw.attach(6);
void loop()
{
  nh.spinOnce();
  delay(1);
}
```


Here is the motor moving with the ROS software
----------------------------------------------
[Robot arm moving with ROS](https://www.youtube.com/watch?v=3TiCBh8qIgg)

![Step14 Image][Image14]

[Image14]: https://github.com/jpallent/roco222/blob/master/arm.jpg "basic commutator"


Improvements
============
If I was to do this project again I would deffinitely change a few things. 
* For the motor I would use an iron core instead of the 3d printed one as explained earlier. I would also add more winding to the coil and maybe more coils. Another thing I would change was the brushes, I would like to think of a better more reliable way to make brushes.

* For the encoder I would of liked to have spend more time on it to try and figure out why ares was having problems as no other group had thoses problems. 

* For the arm project I would redesign some of the parts for example the base needs to be wider to support the arm, then bottom arm piece corners needed to be rounded off, and the cogs for the gear need to be designed better and have support at the top as they kept pushing each other away and this made the claw stop. also i would try make them lighter by making them thinner and have less infil so the servos didnt struggle as much, I also need to give thing some more tolerence when designing the parts so they fit in the holes.

* For the Arm I would of liked to get all the servos connected but unfortuantly we ran out of time.
