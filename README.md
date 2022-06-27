



##### version 0.0.1-4 updated June, 2022

Fork this repo, fill in your markdown and <html> for the 15 slides (max 20 slides), record your presentation and save it as ```recorded-talk.m4a``` (or change the code to reflect the new name.)
 
 Setup gitPages --> settings-->pages-->none to master-->save--> copy the link and replace below.

Demo website of this Github Markdown can be viewed at this GitPages site (replace this link with your Gitpages link) [https://hpssjellis.github.io/my-robotics-machine-learning-teaching-lightning-talk-pecha-kucha/](https://hpssjellis.github.io/my-robotics-machine-learning-teaching-lightning-talk-pecha-kucha/)


This Github Repository [https://github.com/hpssjellis/my-robotics-machine-learning-teaching-lightning-talk-pecha-kucha](https://github.com/hpssjellis/my-robotics-machine-learning-teaching-lightning-talk-pecha-kucha)

Number of Slides: <input type="text" id="myCountLinks" size="6" value="15" >, Seconds per Slide: <input type="text" id="myCountMax" size="6" value="20" >

<div id="myNumSlides" style=" position:sticky; top:0px; left:20px; height:25px; "> ...</div>  <br>

  









<div id="myStick"  style=" position:sticky; top:30px; display:inline; ">
 
 <input type=button value="Start-No-Sound" onclick="{
   document.getElementById('myStick').style.display = 'none';                                                 
   xSlide  = document.getElementById('myCountLinks').value; 
   myMainNum = document.getElementById('myCountMax').value;    
   myAudio01.pause();
   myAudio01.currentTime = 0;  
   myIndex = 0;  
   clearInterval(myLooper);  
   myCountUp = -1;
   carousel();  
}">
 
<input type=button value="Start-Pre-Recorded" onclick="{                                                        
   document.getElementById('myStick').style.display = 'none';   
   xSlide  = document.getElementById('myCountLinks').value; 
   myMainNum = document.getElementById('myCountMax').value;  
   myAudio01.pause();
   myAudio01.currentTime = 0;                                                
   myAudio01 = new Audio('recorded-talk.m4a');
   myAudio01.play(); 
   myIndex = 0;  
   clearInterval(myLooper);  
   carousel();                                                
}">  
 
  <input type=button value="Rewind" onclick="{
   myIndex = 0;  
   clearInterval(myLooper);
   clearInterval(myCounting);
   if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
      } else {
         myAudio01.pause();
     }
}">   

 <input type=button value="-" onclick="{
   clearInterval(myLooper);
   clearInterval(myCounting);
   myIndex -= 1;    
   window.location.href='#'+myIndex;
}">   
  
<input type=button value="+" onclick="{
  clearInterval(myLooper);
  clearInterval(myCounting);
  myIndex += 1;  
  window.location.href='#'+myIndex;
}"> 
  
<input type=button value="Back" onclick="{
   myIndex = myIndex - 2;    
   if (myIndex <= 0){myIndex=0};                                      
   myNext();
}">   
  
<input type=button value="Next" onclick="{
   myNext();
}"> 
 
    
  
 <input id="myPause" type=button value="Pause" onclick="{ 
   clearInterval(myLooper);
   clearInterval(myCounting);
   if (this.value == 'Pause'){                                                     
       this.value = 'Play / Pause'; 
       if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
      } else {
         myAudio01.pause();
     }
   } else {    
     myIndex -= 1; 
     myCountUp += 1;
     carousel();                                                 
     this.value = 'Pause';  
     if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
         myAudio01.play();
      }                                                    
   }
}"> 
 
<input type=button value="Hide" onclick="{
   document.getElementById('myStick').style.display = 'none';
}"> 
  <input type=button value="TOP" onclick="{ 
   window.location.href='#top'; 
}">  
  
 </div>

#### 1
# Intro: Lightning Talks in Pecha Kucha Format 

### ~15 Slides, 20 seconds per Slide works out to about 5 min per presenter
### Traditional Format: Powerpoint, PDF,
### But Coders use Github
### So I made the Github README.md file work with Javascript


<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>


#### 2
# Who:

### I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a>
### <a href="https://github.com/hpssjellis?tab=repositories"> Github Profile</a>
### Canadian High School Technology Teacher, with Greater than 30 years teaching Coding. 
### Presently teaching Animation, Coding, 3D Printing and Robotics with Machine Learning 

### I started my Data Science interest when I tried to understand why I couldn't play an instrument very well. <a href="https://rocksetta.com/">https://rocksetta.com/</a>. this project is ongoing :) 
### In the 1990's I was dsigning fully connected Neural Networks. (Not that hard to program), but they never worked for me, So I did other things until until Tensorflow was made public in 2015.
 
 
 
 
 
<!--   Keep for reference
Show how to do images and links. Note: To get the url just paste an image right here

<img src="https://user-images.githubusercontent.com/5605614/175780835-2b0d64a4-0ba8-4c90-9f05-fb4e89cd6980.png" width=700 />

[https://github.com/hpssjellis](https://github.com/hpssjellis)

-->

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>


#### 3
# Future: 
 
### I believe all educated people should have some form of hands on Robotics and Machine Learning Education. It doesn't matter if you are at University to become a Lawyer, Accountant, Scientist, Educator or any field.  Machine Learning is here to have an enormous effect both good and bad on all areas of our lifes. Knowing how Deep Learning works might be the most important thing Educators teach.

 

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>


#### 4
# <a href="https://keras.io/">Keras</a>, <a href="https://www.tensorflow.org/">Tensorflow</a> , <a href="https://pytorch.org/">Pytorch</a>, <a href="https://theano-pymc.readthedocs.io/en/latest/introduction.html">Theano</a> ...
 
### The traditional way to teach Machine Learning and the subset Deep Learning is with these platforms. Mainly for students with some advanced Math skills. These platforms typically involve only the computer and not directly using sensors and/or sending output to actuators. Typically a known dataset is loaded and the Machine Learning model is manipulated to demonstrate understanding of the concept with the output generated for the computer screen. 

 ### Note: <a href="https://gitpod.io/">https://gitpod.io/</a> can help enorously with teaching the above as most Github sites can be loaded into Gitpod (an online Browser docker) and ran with only a few starting commands. With a github login you just need to add to the front of a github URL ``` gitpod.io/#  ```
 
 ### My Gitpod  (old) examples are <a href="https://hpssjellis.github.io/rocksetta-gitpod-links/">rocksetta-gitpod-links</a>

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 5
# <a href="https://store-usa.arduino.cc/products/arduino-tiny-machine-learning-kit">Arduino Tiny Machine Learning Kit</a>
 
### Very well supported by both Harvard SEAS (School of Engineering and Applied Science) Education <a href="http://tinyml.seas.harvard.edu/">TinyMLEdu</a>  The Github at <a href="https://github.com/tinyMLx/courseware/tree/master/edX">tinyMLx Github</a>
 
### Also by <a href="https://edgeimpulse.com/university">EdgeImpulse University</a> Github of the course at <a href="https://github.com/edgeimpulse/courseware-embedded-machine-learning">courseware-embedded-machine-learning</a>
 
### Often a univeresity can get a few free sets of the Arduino Tiny Machine Learning Kit or other hardware from either of these groups.

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 6
# My Maker100 

### For the <a href="https://store-usa.arduino.cc/products/portenta-h7">Arduino PortentaH7</a> with the <a href="https://store-usa.arduino.cc/products/arduino-portenta-vision-shield-lora%C2%AE">LoRa Vision Shield</a> and <a href="https://www.seeedstudio.com/Seeeduino-XIAO-Pre-Soldered-p-4747.html">Seeedstudio XIAO </a>  Github of my course at <a href="https://github.com/hpssjellis/maker100">https://github.com/hpssjellis/maker100</a>

### My main Robotics and Machine Learning course is called <a href="https://github.com/hpssjellis/maker100">Maker 100</a> and is fully on Github, with plans to make all parts available for indivdual purchase and a fully online componenet for technologically capable teenagers to follow before going to University.

### I belive that Machine Learning needs to be taught within an undersgtanding of Roboitcs sensors (flex, touch, light...), actuators (DC motors, stepper, servo, LED's... ), communication (Ethernet, WiFI, BLE, LoRa) and pcb design. So this course quickly touches on all these areas and leaves more advanced topics to the as yet not develpped <a href="https://github.com/hpssjellis/maker101">Maker101</a> course.

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 7
# <a href="https://www.amazon.ca/Raspberry-Model-2019-Quad-Bluetooth/dp/B07TD42S27">Raspberry Pi 4B</a>
 
### All RPI's and other single board computers such as the <a href="https://www.seeedstudio.com/NVIDIA-Jetson-Nano-2GB-Developer-Kit-Wireless-Adapter-Included-p-4707.html">NVIDIA® Jetson Nano™ 2GB Developer Kit </a> 


<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 8
# <a href="https://www.tensorflow.org/js/">TensorflowJS</a> Can reach a large Web capable audience

### In 2017 TensorflowJS was introduced originally as deeplearnJS, using TypeScript and some Compiler Javascript. I spent a lot of time converting the @Google Brain code for Single page Vanilla Javascript that might students could use without installing anything, <a href="https://hpssjellis.github.io/beginner-tensorflowjs-examples-in-javascript/">beginner-tensorflowjs-examples-in-javascript</a>

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>
#### 9
# TinyML should be inexpensive
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 10
# New Hardware 2023
 
 
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 11
# WebSerial Possible Teaching Potential
 
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 1
# Maker101 Model Manipulation and After Classification Analysis
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 13
## Other Boards
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 14
 ## <a href="https://www.voltera.io/">Voltera.io </a> PCB Making
 
### The chip shortage is really making it obvious that making PCB's is a necessary skill tht has many global dependencies.
 
### <a href="https://www.voltera.io/">Voltera.io </a> is a possible educational solution, similar to a 3D printer, but for PCB's. Takes a set size small board, drills wholes, prints traces, manual connect Vias, print solder paste, manual place SMD's (surface mount components), auto heat, long cool down. Uses very low temperature silver solder for Through-hole-technology (THT) components.
 
 ### I have asked my school to purchase a V-One, but the $6000 USD price tag might be to steep. Perhaps someone hass a suggestion for how to get a grant to get one of these.
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 15
## Exit
 
 ### I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a> Canadian High School Technology Teacher
 
 ### <a href="https://github.com/hpssjellis?tab=repositories"> Github Profile</a>
 ### <a href="https://ca.linkedin.com/in/jeremy-ellis-4237a9bb">Linkedin </a>  
 ### Use this information at your own risk!
 
 ### Unlike a Powerpoint presentation this material can be updated with a newer version as mistakes are corrected or new information becomes available. A new recording of  ```recorded-talk.m4a``` should be made if the changes are substantial.
 
 

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>


<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>



<a href="#top">Top of page</a>





Template for this from https://github.com/hpssjellis/pecha-kucha-lightning-talks-template



### By Jeremy Ellis Twitter @Rocksetta Use at your own Risk!
### Note when looking at the markdown none of the javascript buttons appear, you must go to your Gitpages Demo Link!
A few Javascript abilites do not work, such as hiding the code. So all the Javascript not in buttons is below. 



<script>
 let myIndex = 1;
 let myLooper = 0;
 let myCounting = 0;
 let myMainNum = 20;   
 let myCountUp = 0;
 let xSlide = 3;
 let myAudio01 = new Audio();
 
;
function carousel() {
  clearInterval(myCounting);
  myCountUp = -1;
  var i;
;
  myIndex++;
  if (myIndex > xSlide) {myIndex = xSlide};    
  window.location.href='#'+myIndex;
  myCountDown();
  myCounting = setInterval(myCountDown, 1000);
  myLooper = setTimeout(carousel, myMainNum*1000); 
}
  
function myCountDown(){
  myCountUp++;
  if (myCountUp >= myMainNum ) {
    myCountUp = myMainNum;                              
  }
  if (myIndex >= xSlide && myMainNum == myCountUp){ 
     document.getElementById("myNumSlides").innerHTML = `&nbsp;&nbsp;&nbsp; Slide ${myIndex} of ${xSlide} slides. ALL DONE <input type=button value="Show"  style="height:25px; " onclick="{document.getElementById('myStick').style.display = 'inline'; }"> `;
     clearInterval(myCounting);             
     clearInterval(myLooper);  
  }
  else {    
     document.getElementById("myNumSlides").innerHTML = `&nbsp;&nbsp;&nbsp; Slide ${myIndex} of ${xSlide} slides. ${myMainNum-myCountUp} seconds remaining <input type=button value="Show" style="height:25px; " onclick="{document.getElementById('myStick').style.display = 'inline'; }"> `;
  }
}
;
function myNext(){   
  xSlide  = document.getElementById('myCountLinks').value; 
  myMainNum = document.getElementById('myCountMax').value;                        
  clearInterval(myLooper) ; 
  carousel();  
}  
;
</script>  

