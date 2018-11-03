<!DOCTYPE html>
<meta content='text/html; charset=UTF-8' http-equiv='Content-Type'/>

<html>
<head>
<title>MEGASENA</title>
<style>

div {
    width: 50%;
    margin: auto;
    border: 7.5px ridge yellow;
}
.msg {
    width: 90%;
    margin: auto;
    border: 0px ridge yellow;
}
.num {
    width: 90%;
    margin: auto;
    border: 0px ridge yellow;
}
.mod {
   background-color:black;
   color:yellow;
   text-align:center;
   float: left;
   margin: 7.5px;
   padding: 7.5px;
   width: 25px;
   border: 2.5px ridge yellow;
}

.button {
    background-color: white;
    border: double;
    color: black;
    padding: 2px 6px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    -webkit-transition-duration: 0.4s; 
    transition-duration: 0.5s;
    cursor: pointer;
}

.button1 {
   border-radius: 25px;
}

.button:hover {
    background-color: #555555;
    color: white;
}
.button:active {
  background-color: #555555;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
a:link {
    color: yellow;
    background-color: transparent;
    text-decoration: none;
}
a:visited {
    color: yellow;
    background-color: transparent;
    text-decoration: none;
}
a:active {
    color: yellow;
    background-color: transparent;
    text-decoration: underline;
} 
</style>
</head>
<body onload="GeraDez()">

<script>

var NUM = [], stt, NEA, NN, str, STATUS, X = 6;

function INICIO() {
   if (NEA) {
   document.getElementById("XX00").innerHTML = "AGUARDE . . .";
   setTimeout(RELOAD, 1500);   
}
   else {
   MEGA();}
}
function GeraDez() {
   var W;
    var txt = " ";
    var NMR = [6,7,8,9,10,11,12,13,14,15];
    for (W = 0; W < NMR.length; W++) {
   if (NMR[W] < 10) { NMR[W] = "0" + NMR[W]; }
    txt += "<div class='mod'>"+"<a href=javascript:pegadez("+NMR[W]+")>" + NMR[W] + "</a>" + "</div>";
    }
    document.getElementById("00").innerHTML = txt;
   document.getElementById("XX00").innerHTML = " QUANTAS DEZENAS? ";
}

function pegadez(dez) {
   X = dez;
}

A
function MEGA() {
   NN = (Math.floor(Math.random() * 60)+1);
if (NN < 10) {
   NN = "0" + NN;
}
   
   str = document.getElementById("H00").innerHTML = NUM.toString();
  
   document.getElementById("H00").innerHTML = "";     

   
    var pos = str.search(NN);
if (pos == -1) {
   
    NUM.push(NN)
   
    document.getElementById("H01").innerHTML += "<hr>"+NN;
   
    NEA = NUM.length;
}
if (NEA < X) {
   STATUS = "ON";
    var LOOPING = setTimeout(MEGA, 750);
}
else {
   STATUS = "OFF";
   var FIM = setTimeout(LHORIZ, 1000);
}
   document.getElementById("00").innerHTML = " GERANDO PALPITES ";
   document.getElementById("XX00").innerHTML = " " + NEA + "ª " + "DEZENA";
}


function RELOAD() {
   window.location.reload(true);
}

function LHORIZ() {
   document.getElementById("H01").innerHTML += "<hr>";
   document.getElementById("XX00").innerHTML = "* BOA SORTE! *";
   document.getElementById("XX01").innerHTML = "Victor Blenndon"
   document.getElementById("00").innerHTML = "";
}
</script>

<br>
<div align="center">
<h2 ID="XX00" style="color:black;"></h2>


<div class='num'>
<h3 id="00" align="center"></h3>
</div>

<div class='msg'>
<h2 ID="XX01" style="color:blue;"></h2>
</div>
<button class="button button1" onclick="INICIO()"><b>INICIAR</b></button>
</div>

<p id="H00"></p>
<h1 id="H01" align="center"></h1>
<h3 id="01" align="left" style="color:black;"></h3>
</body>
</html>
