# SS-DYNAMIC-SENSEI-BORONG-CHINA
"We Help You Buy Any Products Items From China🇨🇳🇲🇾"
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>SS DYNAMIC SENSEI BORONG CHINA</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Segoe UI,sans-serif;
}

body{
background:#0d0d0d;
color:white;
}

header{
background:
linear-gradient(rgba(0,0,0,.75),rgba(0,0,0,.75)),
url('https://images.unsplash.com/photo-1521295121783-8a321d551ad2');
background-size:cover;
background-position:center;
padding:100px 20px;
text-align:center;
}

header h1{
font-size:55px;
color:#ff0000;
}

header h2{
margin-top:15px;
color:#ffffff;
}

.container{
max-width:1200px;
margin:auto;
padding:50px 20px;
}

.card{
background:#151515;
padding:25px;
border-radius:15px;
margin-bottom:25px;
border:1px solid #333;
}

.card h2{
color:#ff4444;
margin-bottom:15px;
}

input,textarea{
width:100%;
padding:12px;
margin:8px 0;
border:none;
border-radius:8px;
background:#222;
color:white;
}

button{
background:#ff0000;
color:white;
border:none;
padding:15px;
width:100%;
border-radius:8px;
cursor:pointer;
font-weight:bold;
}

button:hover{
background:#cc0000;
}

.result{
margin-top:15px;
padding:10px;
background:#222;
border-radius:8px;
}

.whatsapp{
position:fixed;
right:20px;
bottom:20px;
background:#25D366;
padding:15px 20px;
border-radius:50px;
color:white;
text-decoration:none;
font-weight:bold;
}

footer{
background:#111;
padding:30px;
text-align:center;
}

</style>
</head>

<body>

<header>

<h1>SS DYNAMIC SENSEI BORONG CHINA</h1>

<h2>
WE HELP MANAGE THE PURCHASE AND DELIVERY OF YOUR PRODUCTS
FROM 🇨🇳 CHINA TO 🇲🇾 MALAYSIA
</h2>

</header>

<div class="container">

<div class="card">

<h2>PRODUCT REQUEST FORM</h2>

<input type="text" id="name" placeholder="Customer Name">
<input type="text" id="phone" placeholder="WhatsApp Number">
<input type="email" id="email" placeholder="Email">
<input type="text" id="product" placeholder="Product Name / Product Link">
<input type="number" id="weight" placeholder="Weight (KG)">
<input type="number" id="length" placeholder="Length (CM)">
<input type="number" id="width" placeholder="Width (CM)">
<input type="number" id="height" placeholder="Height (CM)">

<button onclick="sendWA()">
SUBMIT TO WHATSAPP
</button>

</div>

<div class="card">

<h2>PRODUCT SEARCH ENGINE</h2>

<input type="text" id="productLink"
placeholder="Paste Product Link Here">

<button onclick="window.open(document.getElementById('productLink').value)">
OPEN PRODUCT LINK
</button>

</div>

<div class="card">

<h2>RMB ↔ MYR CONVERTER</h2>

<input type="number" id="rmb"
placeholder="RMB">

<button onclick="convertRMB()">
CONVERT TO MYR
</button>

<div class="result" id="rmbResult"></div>

</div>

<div class="card">

<h2>CBM CALCULATOR</h2>

<input type="number" id="l"
placeholder="Length CM">

<input type="number" id="w"
placeholder="Width CM">

<input type="number" id="h"
placeholder="Height CM">

<button onclick="calculateCBM()">
CALCULATE CBM
</button>

<div class="result" id="cbmResult"></div>

</div>

<div class="card">

<h2>VOLUMETRIC WEIGHT</h2>

<input type="number" id="vl"
placeholder="Length CM">

<input type="number" id="vw"
placeholder="Width CM">

<input type="number" id="vh"
placeholder="Height CM">

<button onclick="calculateVol()">
CALCULATE VOLUMETRIC
</button>

<div class="result" id="volResult"></div>

</div>

<div class="card">

<h2>AIR SHIPPING COST</h2>

<input type="number" id="airkg"
placeholder="Weight KG">

<input type="number" id="airrate"
placeholder="Rate Per KG">

<button onclick="airCost()">
CALCULATE
</button>

<div class="result" id="airResult"></div>

</div>

<div class="card">

<h2>SEA SHIPPING COST</h2>

<input type="number" id="cbm"
placeholder="CBM">

<input type="number" id="cbmrate"
placeholder="Rate Per CBM">

<button onclick="seaCost()">
CALCULATE
</button>

<div class="result" id="seaResult"></div>

</div>

</div>

<footer>

<h3>SS DYNAMIC SENSEI BORONG CHINA</h3>

<p>
Taobao • 1688 • Pinduoduo • JD • Tmall • Xianyu
</p>

</footer>

<a href="https://wa.me/601151453147"
class="whatsapp">
WhatsApp Now
</a>

<script>

function sendWA(){

let msg=
"*SS DYNAMIC SENSEI BORONG CHINA*%0A%0A"+
"Name: "+name.value+"%0A"+
"Phone: "+phone.value+"%0A"+
"Email: "+email.value+"%0A"+
"Product: "+product.value+"%0A"+
"Weight: "+weight.value+" KG";

window.open(
"https://wa.me/601151453147?text="+msg
);

}

function convertRMB(){

let rmb=parseFloat(document.getElementById("rmb").value);

let rate=0.66;

let myr=rmb/rate;

document.getElementById("rmbResult")
.innerHTML="MYR : RM "+myr.toFixed(2);

}

function calculateCBM(){

let l=document.getElementById("l").value;
let w=document.getElementById("w").value;
let h=document.getElementById("h").value;

let cbm=(l*w*h)/1000000;

document.getElementById("cbmResult")
.innerHTML="CBM = "+cbm.toFixed(4);

}

function calculateVol(){

let l=document.getElementById("vl").value;
let w=document.getElementById("vw").value;
let h=document.getElementById("vh").value;

let vol=(l*w*h)/6000;

document.getElementById("volResult")
.innerHTML="Volumetric Weight = "
+vol.toFixed(2)+" KG";

}

function airCost(){

let kg=document.getElementById("airkg").value;
let rate=document.getElementById("airrate").value;

document.getElementById("airResult")
.innerHTML="RM "+(kg*rate).toFixed(2);

}

function seaCost(){

let cbm=document.getElementById("cbm").value;
let rate=document.getElementById("cbmrate").value;

document.getElementById("seaResult")
.innerHTML="RM "+(cbm*rate).toFixed(2);

}

</script>

</body>
