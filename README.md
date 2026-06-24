# SS-DYNAMIC-SENSEI-BORONG-CHINA
"We Help You Buy Any Products Items From China🇨🇳🇲🇾"
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SS DYNAMIC SENSEI BORONG CHINA</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:#0a0a0a;
color:#fff;
}

header{
background:linear-gradient(135deg,#8B0000,#ff0000,#111);
padding:80px 20px;
text-align:center;
}

header h1{
font-size:50px;
}

header p{
margin-top:15px;
font-size:18px;
}

.container{
max-width:1200px;
margin:auto;
padding:40px 20px;
}

.card{
background:#111;
padding:25px;
margin-bottom:25px;
border-radius:15px;
border:1px solid #333;
}

h2{
color:#ff4444;
margin-bottom:20px;
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
width:100%;
padding:15px;
background:#ff0000;
color:white;
border:none;
border-radius:8px;
font-size:18px;
cursor:pointer;
}

button:hover{
background:#cc0000;
}

.result{
background:#1a1a1a;
padding:15px;
margin-top:10px;
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
</style>

</head>
<body>

<header>
<h1>SS DYNAMIC SENSEI BORONG CHINA</h1>

<p>
WE HELP MANAGE THE PURCHASE AND DELIVERY OF YOUR PRODUCTS ITEMS
FROM 🇨🇳 CHINA TO 🇲🇾 MALAYSIA
</p>

</header>

<div class="container">

<div class="card">

<h2>Product Request Form</h2>

<input type="text" id="name" placeholder="Customer Name">

<input type="text" id="phone" placeholder="WhatsApp Number">

<input type="email" id="email" placeholder="Email">

<input type="text" id="product"
placeholder="Product Name or Product Link">

<input type="number" id="weight"
placeholder="Weight (KG)">

<input type="number" id="length"
placeholder="Length (CM)">

<input type="number" id="width"
placeholder="Width (CM)">

<input type="number" id="height"
placeholder="Height (CM)">

<button onclick="sendWhatsApp()">
SEND TO WHATSAPP
</button>

</div>

<div class="card">

<h2>Product Search Engine</h2>

<input type="text"
placeholder="Paste Taobao / 1688 / Pinduoduo / Tianmao / Jingdong / Xianyu Link">

<div class="result">
Copy & Paste Product Link Here
</div>

</div>

<div class="card">

<h2>RMB ↔ MYR Converter</h2>

<input type="number" id="rmb"
placeholder="RMB">

<button onclick="convertRMB()">
Convert RMB To MYR
</button>

<div id="rmbResult" class="result"></div>

<p>
XE.com | Wise.com | WesternUnion.com
</p>

</div>

<div class="card">

<h2>Volumetric Calculator</h2>

<input type="number" id="vlength"
placeholder="Length CM">

<input type="number" id="vwidth"
placeholder="Width CM">

<input type="number" id="vheight"
placeholder="Height CM">

<button onclick="calculateVolumetric()">
Calculate Volumetric Weight
</button>

<div id="volResult" class="result"></div>

</div>

<div class="card">

<h2>CBM Calculator</h2>

<input type="number" id="clength"
placeholder="Length CM">

<input type="number" id="cwidth"
placeholder="Width CM">

<input type="number" id="cheight"
placeholder="Height CM">

<button onclick="calculateCBM()">
Calculate CBM
</button>

<div id="cbmResult" class="result"></div>

</div>

<div class="card">

<h2>Shipping Cost Estimator</h2>

<input type="number" id="shipkg"
placeholder="Weight KG">

<button onclick="estimateShipping()">
Estimate Shipping
</button>

<div id="shipResult" class="result"></div>

</div>

</div>

<a class="whatsapp"
href="https://wa.me/601151453147"
target="_blank">
WhatsApp
</a>

<script>

function sendWhatsApp(){

let msg =
"*SS DYNAMIC SENSEI BORONG CHINA*%0A%0A"+
"Name: "+name.value+"%0A"+
"WhatsApp: "+phone.value+"%0A"+
"Email: "+email.value+"%0A"+
"Product: "+product.value+"%0A"+
"Weight: "+weight.value+" KG";

window.open(
"https://wa.me/601151453147?text="+msg,
"_blank"
);

}

function convertRMB(){

let rmb=parseFloat(
document.getElementById('rmb').value);

let rate=0.65;

let myr=rmb*rate;

document.getElementById('rmbResult')
.innerHTML=
rmb+" RMB = RM "+myr.toFixed(2);

}

function calculateVolumetric(){

let l=parseFloat(vlength.value);
let w=parseFloat(vwidth.value);
let h=parseFloat(vheight.value);

let result=(l*w*h)/6000;

volResult.innerHTML=
"Volumetric Weight: "+
result.toFixed(2)+" KG";

}

function calculateCBM(){

let l=parseFloat(clength.value);
let w=parseFloat(cwidth.value);
let h=parseFloat(cheight.value);

let cbm=(l*w*h)/1000000;

cbmResult.innerHTML=
"CBM = "+cbm.toFixed(4);

}

function estimateShipping(){

let kg=parseFloat(shipkg.value);

let air=kg*18;
let sea=kg*8;

shipResult.innerHTML=
"Air Freight: RM "+air.toFixed(2)+
"<br>Sea Freight: RM "+
sea.toFixed(2);

}

</script>

</body>
