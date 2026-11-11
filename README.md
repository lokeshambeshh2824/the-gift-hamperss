# the-gift-hamperss
The Gift Hampers Online Shopping Website

<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Gift Hampers - Online Gift Store</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#faf7f2;color:#282019}
header{background:#17120f;color:white;text-align:center;padding:20px}
.logo{font-family:Georgia,serif;font-size:29px;color:#e9c58b}
header p{font-size:10px;letter-spacing:3px}
nav{background:#30231a;padding:13px;text-align:center;position:sticky;top:0;z-index:5}
nav a{color:white;text-decoration:none;margin:0 10px;font-size:13px}
.hero{padding:65px 15px;text-align:center;color:white;background:linear-gradient(#0009,#0009),url('https://images.unsplash.com/photo-1549465220-1a8b9238cd48?w=1200') center/cover}
.hero h1{font:42px Georgia,serif;color:#f0cb91}
.hero p{line-height:1.7}
.btn{background:#d5aa69;color:#24180d;border:0;padding:12px 18px;border-radius:6px;font-weight:bold;cursor:pointer}
section{padding:35px 15px;max-width:1100px;margin:auto}
h2{text-align:center;font:30px Georgia,serif}
.sub{text-align:center;color:#766b60}
.categories{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
.category{background:white;padding:20px;text-align:center;border:1px solid #eadfce;border-radius:9px}
.products{display:grid;grid-template-columns:repeat(3,1fr);gap:15px}
.product{background:white;border:1px solid #eadfce;border-radius:10px;overflow:hidden}
.product img{width:100%;height:180px;object-fit:cover}
.info{padding:12px}
.info h3{font-family:Georgia,serif}
.price{font-weight:bold;color:#a16e2e;margin:10px 0}
.info button{width:100%}
.cart{background:white;border:1px solid #eadfce;border-radius:10px;padding:15px}
.cart-item{display:flex;justify-content:space-between;gap:10px;border-bottom:1px solid #eee;padding:10px 0}
.field{width:100%;padding:12px;margin:7px 0;border:1px solid #ddd;border-radius:6px;font-size:15px}
.promo{background:#211914;color:white;text-align:center;padding:30px;border-radius:10px}
footer{background:#17120f;color:white;text-align:center;padding:25px;font-size:13px;line-height:1.8}
footer a{color:#e5bd7d}
@media(max-width:650px){
.products{grid-template-columns:repeat(2,minmax(0,1fr));gap:9px}
.product img{height:130px}
.info{padding:9px}
.info h3{font-size:15px}
.hero h1{font-size:34px}
nav a{margin:0 5px;font-size:12px}
}
</style>
</head>
<body>

<header>
<div class="logo">The Gift Hampers</div>
<p>PREMIUM PERSONALIZED GIFTS</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#products">Shop</a>
<a href="#cart">Cart</a>
<a href="#contact">Contact</a>
</nav>

<div class="hero" id="home">
<h1>Make Every Moment Special</h1>
<p>आपके अपनों के लिए खूबसूरत और यादगार गिफ्ट हैम्पर्स।</p>
<p>Premium Gifts | Personalised Hampers | Pan India Delivery</p>
<a href="#products"><button class="btn">Shop Now</button></a>
</div>

<section>
<h2>Shop By Category</h2>
<p class="sub">हर खास मौके के लिए खास तोहफा</p>
<div class="categories">
<div class="category">🎂 Birthday Gifts</div>
<div class="category">❤️ Anniversary Gifts</div>
<div class="category">🧸 Couple Gifts</div>
<div class="category">🎁 Premium Hampers</div>
</div>
</section>

<section id="products">
<h2>Our Best Sellers</h2>
<p class="sub">आपके लिए चुने गए खूबसूरत गिफ्ट</p>
<div class="products" id="productList"></div>
</section>

<section id="cart">
<h2>Your Shopping Cart</h2>
<div class="cart">
<div id="cartItems">आपका कार्ट खाली है।</div>
<h3 id="total">Total: ₹0</h3>
<h3>Delivery Details</h3>
<input class="field" id="customer" placeholder="आपका नाम">
<input class="field" id="phone" placeholder="मोबाइल नंबर" type="tel">
<textarea class="field" id="address" placeholder="पूरा डिलीवरी पता"></textarea>
<button class="btn" style="width:100%" onclick="orderNow()">Order on WhatsApp</button>
</div>
</section>

<section>
<div class="promo">
<h2>Make Someone Smile ❤️</h2>
<p>आपका प्यार, हमारा खूबसूरत गिफ्ट।</p>
<p>Pan India Delivery Available</p>
</div>
</section>

<section id="contact">
<h2>Contact Us</h2>
<p class="sub">ऑर्डर और जानकारी के लिए WhatsApp करें</p>
<center>
<a href="https://wa.me/917725974382" target="_blank">
<button class="btn">WhatsApp: 7725974382</button>
</a>
</center>
</section>

<footer>
<div class="logo">The Gift Hampers</div>
Premium Curated Personalized Gifts<br>
Pan India Delivery Available<br>
© 2026 The Gift Hampers. All Rights Reserved.
</footer>

<script>
const products=[
{id:1,name:"Luxury Birthday Hamper",price:999,img:"https://images.unsplash.com/photo-1549465220-1a8b9238cd48?w=600"},
{id:2,name:"Chocolate Gift Box",price:599,img:"https://images.unsplash.com/photo-1548907040-4d42f6e9c7b2?w=600"},
{id:3,name:"Teddy Bear Hamper",price:799,img:"https://images.unsplash.com/photo-1559454403-b8fb88521f11?w=600"},
{id:4,name:"Rose Gift Hamper",price:899,img:"https://images.unsplash.com/photo-1494972308805-463bc619d34e?w=600"},
{id:5,name:"Premium Couple Hamper",price:1299,img:"https://images.unsplash.com/photo-1513201099705-a9746e1e201f?w=600"},
{id:6,name:"Personalized Gift Box",price:699,img:"https://images.unsplash.com/photo-1607344645866-009c320c5ab8?w=600"}
];

let cart=[];

function showProducts(){
document.getElementById("productList").innerHTML=products.map(p=>`
<div class="product">
<img src="${p.img}" alt="${p.name}" loading="lazy">
<div class="info">
<h3>${p.name}</h3>
<div class="price">₹${p.price}</div>
<button class="btn" onclick="addToCart(${p.id})">Add to Cart</button>
</div>
</div>`).join("");
}

function addToCart(id){
let item=cart.find(x=>x.id===id);
if(item){item.qty++}
else{cart.push({...products.find(x=>x.id===id),qty:1})}
showCart();
alert("Product cart में जोड़ दिया गया!");
}

function changeQty(id,change){
let item=cart.find(x=>x.id===id);
if(!item)return;
item.qty+=change;
if(item.qty<=0)cart=cart.filter(x=>x.id!==id);
showCart();
}

function showCart(){
let box=document.getElementById("cartItems");
if(cart.length===0){
box.innerHTML="आपका कार्ट खाली है।";
}else{
box.innerHTML=cart.map(x=>`
<div class="cart-item">
<div>${x.name}<br>₹${x.price} × ${x.qty}</div>
<div>
<button onclick="changeQty(${x.id},-1)">−</button>
${x.qty}
<button onclick="changeQty(${x.id},1)">+</button>
</div>
</div>`).join("");
}
let total=cart.reduce((sum,x)=>sum+x.price*x.qty,0);
document.getElementById("total").innerText="Total: ₹"+total;
}

function orderNow(){
if(cart.length===0){alert("पहले कोई प्रोडक्ट चुनें।");return}
let name=document.getElementById("customer").value.trim();
let phone=document.getElementById("phone").value.trim();
let address=document.getElementById("address").value.trim();

if(!name||!phone||!address){
alert("कृपया नाम, मोबाइल नंबर और पता भरें।");
return;
}
if(!/^[0-9]{10}$/.test(phone)){
alert("कृपया 10 अंकों का मोबाइल नंबर डालें।");
return;
}

let total=cart.reduce((sum,x)=>sum+x.price*x.qty,0);
let message="Hello The Gift Hampers! मुझे ऑर्डर करना है:%0A%0A";
cart.forEach(x=>{
message+=encodeURIComponent(x.name+" x "+x.qty+" = ₹"+(x.price*x.qty))+"%0A";
});
message+="%0A"+encodeURIComponent("Total: ₹"+total);
message+="%0A"+encodeURIComponent("Name: "+name);
message+="%0A"+encodeURIComponent("Phone: "+phone);
message+="%0A"+encodeURIComponent("Address: "+address);

window.open("https://wa.me/917725974382?text="+message,"_blank");
}

showProducts();
showCart();
</script>
</body>
</html>
