



##### version 0.0.3-8 updated June, 2022

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

### ~15 slides, 20 seconds per slide works out to about 5 min per presenter
### Traditional Business/Education Format: Powerpoint, PDF (Issue for audience not able to click links)
### But Coders use Github!
### So I made a Github README.md file that works with Javascript for both audio and automatic scrolling


<br><br><br><br><br><br><br><br><br>
<hr>


#### 2
# Who:

### I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a>
### <a href="https://github.com/hpssjellis?tab=repositories"> Github Profile</a>
### Canadian High School Technology Teacher, with greater than 30 years experience teaching coding. 
### Presently teaching Animation, Coding, 3D Printing and Robotics with Machine Learning 

### I started my Data Science interests when I tried to understand patterns in music and developed a sing-able music notation. <a href="https://rocksetta.com/">https://rocksetta.com/</a>. This project is ongoing  :smile:
### In the early 1990's I was designing fully connected Neural Networks using Quick Pascal. (Not that hard to program), but they never worked, they just kept oscillating between solutions. I did other things until Tensorflow was made public in 2015. I knew this was something that students would benefit from but has to wait until 2017 when deeplearnJS came out.
 
 
 
 
 
<!--   Keep for reference
Show how to do images and links. Note: To get the url just paste an image right here

<img src="https://user-images.githubusercontent.com/5605614/175780835-2b0d64a4-0ba8-4c90-9f05-fb4e89cd6980.png" width=700 />

[https://github.com/hpssjellis](https://github.com/hpssjellis)

-->

<br><br><br><br><br><br><br>
<hr>


#### 3
# Topic: 
 
### I believe all educated people should have some form of hands on Robotics and Machine Learning Education. It doesn't matter if the person is at University to become a Lawyer, Accountant, Scientist, Educator or any field.  Machine Learning is here to stay, and will have an enormous effect, both good and bad, on all areas of society. Knowing how deep learning works might be the most important thing Educators teach.

### Some ML Educational Issues: 

### Traditional Method is too difficult for the general population and gives no preparation for Embedded devices

### Online Simplifications: (<a href="https://www.edgeimpulse.com/">EdgeImpulse</a>, <a href="https://ide.tinkergen.com/">CodeCraft-tinkergen</a>, <a href="https://scratch.mit.edu/studios/3995548/">Scratch</a>) (Motion, Sound, Vision:Classification and FOMO) Very simple for any age group of students with cell phones to quickly (under 40 minutes) understand how to create a dataset and train a Machine Learning model and test it's effectiveness.
 
### There is a huge gap between the Tranditional and Online teaching methods.
 
### Issues: The Online is simpler but advanced issues are: How to program the embedded device after analysis, how to use other sensors, and ability to do advanced model manipulation. 

<br><br><br><br><br><br><br>
<hr>


#### 4
# <a href="https://keras.io/">Keras</a>, <a href="https://www.tensorflow.org/">Tensorflow</a> , <a href="https://pytorch.org/">Pytorch</a>, <a href="https://theano-pymc.readthedocs.io/en/latest/introduction.html">Theano</a> ...
 
### The traditional way to teach Machine Learning and the subset Deep Learning is with these platforms. Mainly for students with some advanced Math skills. These platforms typically involve only the computer and not directly using sensors and/or sending output to actuators. Typically a known dataset is loaded and the Machine Learning model is manipulated to demonstrate understanding of the concept with the output generated for the computer screen. 

### Note: <a href="Gitpod.io">https://gitpod.io/</a> can help enorously with teaching the above as most Github sites can be loaded into Gitpod (an online Browser docker) and ran with only a few starting commands. With a github login you just need to add to the front of a github URL ``` gitpod.io/#  ``` My Gitpod  (old) examples are <a href="https://hpssjellis.github.io/rocksetta-gitpod-links/">rocksetta-gitpod-links</a>
 
![image](https://user-images.githubusercontent.com/5605614/176257845-40bcfdf2-f3e2-4ae3-9ca9-59d7d2b20b35.png)


<br><br><br><br><br><br><br><br><br>
<hr>

#### 5
# EdgeImpulse and the <a href="https://store-usa.arduino.cc/products/arduino-tiny-machine-learning-kit"> Arduino Tiny Machine Learning Kit</a>

### Very well supported by Harvard SEAS (School of Engineering and Applied Science) Education <a href="http://tinyml.seas.harvard.edu/">TinyMLEdu</a>  The Github at <a href="https://github.com/tinyMLx/courseware/tree/master/edX">tinyMLx Github</a>
 
### Also by <a href="https://edgeimpulse.com/university">EdgeImpulse University</a> Github of the course at <a href="https://github.com/edgeimpulse/courseware-embedded-machine-learning">courseware-embedded-machine-learning</a>

 ![image](https://user-images.githubusercontent.com/5605614/176258229-111d35ef-e27f-4c83-9abf-e9e264306b73.png)

### Often a university can get a few free sets of the Arduino Tiny Machine Learning Kits or other hardware from either of these groups.

<br><br><br><br><br><br><br><br>
<hr>

#### 6
# My Maker100 
### For the <a href="https://store-usa.arduino.cc/products/portenta-h7">Arduino PortentaH7</a> with the <a href="https://store-usa.arduino.cc/products/arduino-portenta-vision-shield-lora%C2%AE">LoRa Vision Shield</a> and <a href="https://www.seeedstudio.com/Seeeduino-XIAO-Pre-Soldered-p-4747.html">Seeedstudio XIAO </a>  Github of my course at <a href="https://github.com/hpssjellis/maker100">https://github.com/hpssjellis/maker100</a>

### My main Robotics and Machine Learning course is called <a href="https://github.com/hpssjellis/maker100">Maker 100</a> and is fully on Github, with plans to make all parts available for indivdual equipment purchase and a fully online component for technologically capable teenagers to follow before going to University.

### I belive that Machine Learning needs to be taught within an understanding of Robotic sensors (flex, touch, light...), actuators (DC motors, stepper, servo, LED's... ), communication (Ethernet, WiFI, BLE, LoRa) and PCB design ( best PCB video <a href="https://www.youtube.com/watch?v=gjPNYMRA0m8&list=PLbKMtvtYbdPMZfzGuVTdc0MWKrFvU4nsu&index=3">here</a>). The Maker100 course quickly touches on all these areas and leaves more advanced topics to the as yet not developed <a href="https://github.com/hpssjellis/maker101">Maker101</a> course.

![image](https://user-images.githubusercontent.com/5605614/176285054-ea98ff42-df6e-408a-b7c8-f480d5912d73.png)
<hr>

#### 7
# <a href="https://www.amazon.ca/Raspberry-Model-2019-Quad-Bluetooth/dp/B07TD42S27">Raspberry Pi 4B</a>
### All RPI's and other single board computers such as the <a href="https://www.seeedstudio.com/NVIDIA-Jetson-Nano-2GB-Developer-Kit-Wireless-Adapter-Included-p-4707.html">NVIDIA® Jetson Nano™ 2GB Developer Kit </a> have the advantage of near full computer power with up to 40 pins for connectivity to sensors, actuators and built in Communication. Really the best situation, except for the larger amount of electricity used, hardware cost and larger size compared to other microcontrollers.


<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>


#### 8
# TinyML should be inexpensive
### As Educators we purchase kits that allow students to experience many facets of Robotics and Embedded Machine Learning, however the big picture goal is for student's to be able to design specific combinations of components that they have a Proof of Concept that the components can do the job. The indivisual componenets can be very cheap. The $111 Arduino PortentaH7 chip costs $2.80
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 9
# New Hardware 2023
### What amazing hardware will come out in 2023? Cheaper, smaller, less electricity demands and more or specific connectivity. I am waiting for an inexpensive LoRaWan device.
 
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>
 
 
#### 10
# <a href="https://www.tensorflow.org/js/">TensorflowJS</a> Can reach a large Web capable audience
### In 2017 TensorflowJS was introduced originally as deeplearnJS, using TypeScript and some compiled Javascript. I spent a lot of time converting the @Google Brain code for Single page Vanilla Javascript that student's could use without installing anything, <a href="https://hpssjellis.github.io/beginner-tensorflowjs-examples-in-javascript/">beginner-tensorflowjs-examples-in-javascript</a> In my opinion TensorflowJS is the best, most powerful platform to truely teach Machine Learning to the largest audience. 
 
### Note: I have converted TensorflowJS models to arduino <a href="https://github.com/hpssjellis/my-examples-for-the-arduino-portentaH7/tree/master/m09-Tensoflow/tfjs-convert-to-arduino-header">here</a> but it is a bit complex and size is always an issue, much easier to work with EdgeImpulse!

![image](https://user-images.githubusercontent.com/5605614/176290714-58fa7196-fe53-4ce9-a77b-2687b4e757fa.png)



<hr>
#### 11
# WebSerial Possible Teaching Potential
### WebSerial is an interesting combination of microcontrollers with Javascript webpages such as TensorflowJS and working on Desktop or Android Cell Phone. See demo page <a href="https://hpssjellis.github.io/my-examples-of-arduino-webUSB-webSerial/public/webserial-and-polyfill.html">here</a> which has links to the Arduino files. Teaching power of TensorflowJS, cheap microcontroller to connect with Actuators (to do something), possibly connect with Sensors, but a cell phone has a lot of sensors built in. Interesting potentail here for education with minimal cost.
 ![image](https://user-images.githubusercontent.com/5605614/176287664-bd0f1893-c3df-4f50-bcc4-86091141569f.png)


<hr>

#### 1
# Maker101 Model Manipulation and After Classification Analysis
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 13
## Boards other than the $57.50 <a href="https://store-usa.arduino.cc/products/arduino-tiny-machine-learning-kit">Arduino ML Kit</a> and $111 <a href="https://store-usa.arduino.cc/products/portenta-h7">PortentaH7</a> mentioned earlier)
1. The $5.40 USD [Seeeduino XIAO](https://www.seeedstudio.com/Seeeduino-XIAO-Arduino-Microcontroller-SAMD21-Cortex-M0+-p-4426.html)  Only a limited number of pins, but works with my Arduino MBED code<br><img src="https://user-images.githubusercontent.com/5605614/176248216-7a99f725-e3c6-4698-a1e5-56bfd34dcf54.png" width = 40/><br>
2. The $37 USD [Seeeduino Wio Terminal](https://www.seeedstudio.com/Wio-Terminal-p-4509.html) <br><img src="https://user-images.githubusercontent.com/5605614/176248954-38cad413-3c2d-47cb-84a3-60359ba7e863.png" width = 70/>   
3. The $115.00 USD [NiclaVision](https://store-usa.arduino.cc/products/nicla-vision?selectedStore=us) could be very good for Color Vision, sound and accelerometer Machine Learning <br><img src="https://user-images.githubusercontent.com/5605614/157479032-f93ac6e1-1139-4886-bf40-9dfc6e8c2b9c.png" width = 70/>
4. The $33.40 USD [Nano 33 Ble Sense](https://store.arduino.cc/usa/nano-33-ble-sense-with-headers) is very good for sound and accelerometer Machine Learning <br><img src="https://user-images.githubusercontent.com/5605614/176252302-5f9474d1-07cc-4912-ae73-cc96aaeed92c.png" width = 55/>
5. The $129 USD [Sony Spresense Kit](https://shop.framos.com/us/spresense) with Breakout Board and Camera and now works on the Arduino IDE. Absolutely nothing wrong with this board, I have just not yet got it doing Machine Learning on the Arduino IDE yet. Note: uses LED0, LED1, LED2, LED3 instead of LEDB, LEDG, LEDR <br><img src="https://user-images.githubusercontent.com/5605614/176248308-bad3aaa0-fa86-4b34-9a98-e140af242199.png"  width = 55/>
6. The $25.50 USD [Arduino Nano-RP2040-Connect](https://store.arduino.cc/usa/nano-rp2040-connect-with-headers) Is very new but has lots of potential over the RPI Pico as it has WiFi and BLE onboard and the $4 USD [RPIi Pico](https://www.raspberrypi.org/products/raspberry-pi-pico/) Amazing board for the price. <br><img src="https://user-images.githubusercontent.com/5605614/176248392-4cfa47f3-5533-40eb-a8f6-00b2faef2ae8.png"  width = 20/> 
7. The $25.00 USD [ArducamPico-4ML](https://www.arducam.com/raspberry-pi-pico-machine-learning/) This board looks like it would be perfect for machine learning with a mini screen and camera but I have never got it properly working on the Arduino IDE.<br><img src="https://user-images.githubusercontent.com/5605614/176248456-b4cda708-2995-4f6b-8d02-47915015c2fb.png"  width = 50/> 





<hr>

#### 14
## <a href="https://www.voltera.io/">Voltera.io </a> PCB Making
 
### The chip shortage is really making it obvious that in-house making of PCB's as a necessary skill.
 
### <a href="https://www.voltera.io/">Voltera.io </a> is a possible educational solution, similar to a 3D printer, but for PCB's. Takes a set size small board, drills holes, manual install copper vias, prints traces, print solder paste, manual place SMD's (surface mount components), auto heat, long cool down. Uses very low temperature silver solder for through-hole-technology (THT) components.
 
### I have asked my school to purchase a V-One, but the $6000 USD price tag might be to steep. Perhaps someone has a suggestion for how to get a grant to get one of these?
 
 ![image](https://user-images.githubusercontent.com/5605614/176255114-435ef8c9-1989-4761-ae3b-daebea51492f.png)


<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 15
## Exit
 
### I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a> Canadian High School Technology Teacher
 
### <a href="https://github.com/hpssjellis?tab=repositories"> Github Profile</a>
### <a href="https://ca.linkedin.com/in/jeremy-ellis-4237a9bb">Linkedin </a>  
### Use this information at your own risk!
 

 


<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>






<a href="#top">Top of page</a>





Template for this from <a href="https://github.com/hpssjellis/pecha-kucha-lightning-talks-template">pecha-kucha-lightning-talks-template</a>



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

