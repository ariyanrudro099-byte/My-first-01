# My-first-01
Gg1
<!DOCTYPE html>
<html>
<head>
<title>Goongoon ❤️</title>

<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
body{
margin:0;
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(#ffd1e8,#ff9ac2);
font-family:Arial;
overflow:hidden;
}

.card{
background:white;
padding:30px;
border-radius:25px;
text-align:center;
box-shadow:0 0 40px rgba(0,0,0,.2);
width:300px;
z-index:10;
}

img{
width:120px;
height:120px;
border-radius:50%;
object-fit:cover;
margin-bottom:10px;
}

button{
padding:10px 25px;
border:none;
border-radius:20px;
font-size:16px;
cursor:pointer;
}

#yes{
background:#ff2f78;
color:white;
}

#no{
background:#eee;
position:fixed;
}

.heart{
position:absolute;
font-size:20px;
animation:float 6s linear infinite;
}

@keyframes float{
0%{transform:translateY(100vh);}
100%{transform:translateY(-10vh);}
}
</style>
</head>

<body>

<div class="card">

<img src="goongoon.jpg">

<h2>Goongoon will you be my Valentine?</h2>

<br>

<button id="yes" onclick="yes()">Yes</button>
<button id="no">No</button>

<p style="color:gray">Try pressing NO 😈</p>

</div>

<script>
const no = document.getElementById("no");

function move(){
let x = Math.random() * (window.innerWidth - 80);
let y = Math.random() * (window.innerHeight - 40);
no.style.left = x + "px";
no.style.top = y + "px";
}

// PC
no.addEventListener("mouseover", move);

// Mobile
no.addEventListener("touchstart", move);

function yes(){
document.body.innerHTML="<h1 style='color:white;font-size:40px;text-align:center'>Yayyy 😍<br>Goongoon is my Valentine forever 💖</h1>";
}

// Floating hearts
function heart(){
let h=document.createElement("div");
h.className="heart";
h.innerHTML="❤️";
h.style.left=Math.random()*100+"vw";
h.style.animationDuration=Math.random()*3+3+"s";
document.body.appendChild(h);
setTimeout(()=>h.remove(),6000);
}
setInterval(heart,300);
</script>

</body>
</html>
