



##### version 0.0.1-1

Fork this repo, fill in your markdown and <html> for the 15 slides (max 20 slides), record your presentation and save it as ```recorded-talk.m4a``` (or change the code to reflect the new name.)
 
 Setup gitPages --> settings-->pages-->none to master-->save--> copy the link and replace below.

Demo of this Github Markdown can be viewed at this GitPages site (replace this link with your Gitpages link) [[https://hpssjellis.github.io/javascript-on-markdown/](https://hpssjellis.github.io/july-2022-robotics-teaching-lightning-talk-pecha-kucha/)]([https://hpssjellis.github.io/javascript-on-markdown/](https://hpssjellis.github.io/july-2022-robotics-teaching-lightning-talk-pecha-kucha/))


This Github Repository (replace this link with your Repository Link) [https://github.com/hpssjellis/july-2022-robotics-teaching-lightning-talk-pecha-kucha](https://github.com/hpssjellis/july-2022-robotics-teaching-lightning-talk-pecha-kucha)

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
## Intro: What are Ligthning Talks in Pecha Kucha Format 
 (<= 15 Slides, 20 seconds per Slide) 

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>


#### 2
## I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a>
Canadian >30 Year High School Technology Teacher, Presently teaching Animation, Coding, 3D Printing and Robotics with Machine Learning 

<!--   Keep for reference
Show how to do images and links. Note: To get the url just paste an image right here

<img src="https://user-images.githubusercontent.com/5605614/175780835-2b0d64a4-0ba8-4c90-9f05-fb4e89cd6980.png" width=700 />

[https://github.com/hpssjellis](https://github.com/hpssjellis)

-->

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>


#### 3
## Future: 
 
I believe all educated people should have some hands on Robotics and Machine Learning
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 4
 ## <a href="https://github.com/hpssjellis/maker100">Maker 100</a>
 
My main Robotics and Machine Learning course is called <a href="https://github.com/hpssjellis/maker100">Maker 100</a> and is fully on Github, with plans to make all parts available for indivdual purchase and a fully online componenet for technologically capable teenagers to follow before going to University.
 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 5
## Keras, Tensorflow, Pytorch, Theano ...
 
The traditional way to teach Machine Learning and the subset Deep Learning is with these platforms, which typically involve only the computer and not directly using sensors and sending output to actuators other than the computer screen.

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 6
 ## <a href="https://store-usa.arduino.cc/products/arduino-tiny-machine-learning-kit">Arduino Tiny Machine Learning Kit</a>
 
 Very well supported by both Harvard SEAS at <a href="https://github.com/tinyMLx/courseware/tree/master/edX">tinyMLx Github</a>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 7

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 8

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 9

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 10

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 11

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 12

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 13

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 14

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 15

At 20 seconds per page and 15 slides this would be the end of a 5 min presentation
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 16

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 17

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 18

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 19

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 20

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>






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

