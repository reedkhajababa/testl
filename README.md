<!-- শুরু করলাম। শেষ হয় কিনা জানিনা -->
<html>
<head>
<script src="noname.js">
</script>
<style type="text/css">


#mil{background-color:;width:70px;height:100px;}
#dot3{background-color:;width:30px;height:100px;}
#sec{background-color:;width:60px;height:100px;}
#dot2{background-color:;width:30px;height:100px;}
#min{background-color:;width:70px;height:100px;}
#dot1{background-color:;width:30px;height:100px;}
#hrs{background-color:;width:70px;height:100px;}
#hrb{background-color:;width:70px;height:100px;}


#btn1{box-shadow: 3px 4px 5px 0px #111111;font-size:40px;top:400;width:70px;height:70px;border-radius:80px;left:127;background-color:#013B31;}
#btn2{box-shadow: 3px 4px 5px 0px #111111;font-size:20px;top:400;width:70px;height:70px;border-radius:80px;left:127;background-color:#013B31;}
#btn3{font-size:30px;top:410;width:70px;height:70px;border-radius:10px;left:237;background-color:rgba(10,10,2,0);}
#btn4{font-size:30px;top:405;width:70px;height:70px;border-radius:10px;left:20;background-color:rgba(10,10,2,0);}



#vv{
top:240;
height:150px;
width:300px;
opacity:1;
animation-name:ba;
animation-duration :2s;
animation-iteration-count :1 ;
font-weight:bold;
color:black;
position:fixed;
font-size:40px;
top:230;
overflow:scroll;
height:160px;
width:300px;
border:none;
border-radius:5px;
text-shadow:3px 3px 5px #0277bd;
box-shadow:0px 0px 0px 0px #222222;
}

/* ফন্টের স্টাইল */

font{
font-variant:small-caps ;
color:004d40;
font-size:40px;
font-family:Arial, Helvetica, sans-serif;
font-weight:bolder;
text-shadow:2px 2px 5px black;
box-shadow:0px 0px 0px 0px green;
}


/* বডির স্টাইল */

body{background-color:#323232;}

/* বাটনের স্টাইল */


button{
position:fixed;
outline:none;
border:none;
font-variant:cap;
font-weight:bold;
color:black;
width:70px;
height:70px;
}

/* ইনপুটের স্টাইল */
input{visibility:hidden ;}

</style>
</head>
<body>
<div id="vv"></div>
<font style="">.</font>
<font style="font-size:55px; font-weight:bolder; position:relative; left:270px; top:560px;">watch</font>

<div id="mm"></div>
<!-- বাল বাড়তি জিনিস -->
<div>
<font id="hrb" style="color:A00200;position:relative; top:130; left:0;   position:fixed;"> </font>
<font id="hrs" style="color:A00200;position:relative; top:130; left:20;   position:fixed;">00</font>
<font id="dot1"         style="color:A00200;position:relative; top:130; left:80;  position:fixed;">:</font>
<font id="min" style="color:A00200;position:relative; top:130; left:100;   position:fixed;">00</font>
<font id="dot2"         style="color:A00200;position:relative; top:130; left:155;  position:fixed;">:</font>
<font id="sec" style="color:A00200;position:relative; top:130; left:175;  position:fixed;">00</font>
<font id="dot3"         style="color:A00200;position:relative; top:130; left:231;  position:fixed;">:</font>
<font id="mil" style="color:A00200;position:relative; top:130; left:255;  position:fixed;">00</font><br><br><br>
</div>
<!-- বাল সব বাটন এহানে -->

<button id="btn2" onclick="stop()" >■</button>
<button id="btn1" onclick="start()" > ‣</button>
<button id="btn3" onclick="rpar()">✎</button>
<button id="btn4" onclick="reset()">↺</button><br><br>

<!-- বাল সব ইনপুট এহানে -->


<input id="inc" value="0"></input>
<input id="inb" value="0"></input>
<input id="ina" value="0"></input>
<input id="ind" value="0"></input>

<!-- বালের স্ক্রিপ্ট শুরু -->

<font style="position:fixed;font-size:15px;top:500; left:20;">©NahidZamanReed</font>



<script type="text/javascript">
var ina=document.getElementById("ina");
var inb=document.getElementById("inb");
var inc=document.getElementById("inc");
var ind=document.getElementById("ind");
var minl=document.getElementById("min");
var secl=document.getElementById("sec");
var mill=document.getElementById("mil");
var hrs=document.getElementById("hrs");

//যুগান্তকারী ফাংশন 

function rpar(){ 
document.getElementById("vv").innerHTML += hrs.innerHTML+" : "+ minl.innerHTML+" : "+secl.innerHTML+" : "+mill.innerHTML+ "<br/>";
}


// সেকেন্ডের ফাংশন 
function sec() {
ina.value++;
if (ina.value>99) { ina.value=0; inb.value++;}
if (inb.value>59) { inb.value=0; inc.value++;}
if (inc.value>59) { inc.value=0; ind.value++;}
mill.innerHTML =(ina.value);
secl.innerHTML =(inb.value);
minl.innerHTML =(inc.value);
hrs.innerHTML =(ind.value);
}

// টিপ দিলে শুরু
function start(){
document.getElementById("btn2").disabled= false;
document.getElementById("btn1").disabled= true;
timer=setInterval (sec,10);
$("#btn1").hide();
$("#btn2").show();
}

// টিপ দিলে শেষ
function stop() {
document.getElementById("btn2").disabled= false;
document.getElementById("btn1").disabled= false;
clearInterval(timer);
g=null;
$("#btn2").hide();
$("#btn1").show();
}

// টিপ দিলে রিসেট হইবো
function reset(){
document.getElementById("btn2").disabled= true ;
document.getElementById("btn1").disabled= false;
stop();
ina.value =00;
inb.value=00;
inc.value=00;
mill.innerHTML =0+"0";
secl.innerHTML =0+"0";
minl.innerHTML =0+"0";
hrs.innerHTML =0+"0";
vv.innerHTML =""
}
</script>
</body>
</html>
