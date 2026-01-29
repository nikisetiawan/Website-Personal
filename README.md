WEBSITE RASA NUSANTARA INDONESIA
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Rasa Nusantara | Smart Food Store</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', sans-serif;
}

body {
  background: #f8f8f8;
  color: #111;
}

/* NAVBAR */
.navbar {
  background: #020617;
  color: #fff;
  padding: 20px 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top: 0;
  z-index: 10;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

.logo span {
  color: #facc15;
}

nav a {
  color: #fff;
  text-decoration: none;
  margin-left: 25px;
}

nav a:hover {
  color: #facc15;
}

/* HERO */
.hero {
  height: 80vh;
  background: linear-gradient(rgba(0,0,0,.6),rgba(0,0,0,.6)),
  url("https://images.unsplash.com/photo-1504674900247-0877df9cc836");
  background-size: cover;
  background-position: center;
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 60px;
}

.hero h1 {
  font-size: 48px;
  margin-bottom: 15px;
}

.hero p {
  max-width: 500px;
  margin-bottom: 25px;
}

.hero button {
  width: 220px;
  padding: 15px;
  border: none;
  background: #facc15;
  font-weight: bold;
  border-radius: 5px;
  cursor: pointer;
}

/* SECTION */
section {
  padding: 80px 60px;
}

h2 {
  text-align: center;
  margin-bottom: 40px;
  font-size: 32px;
}

/* PRODUCTS */
.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
}

.product-card {
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 10px 20px rgba(0,0,0,.1);
  overflow: hidden;
}

.product-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.product-card h3,
.product-card p {
  padding: 15px;
}

.product-card button {
  margin: 15px;
  width: calc(100% - 30px);
  padding: 12px;
  border: none;
  background: #020617;
  color: #fff;
  border-radius: 5px;
  cursor: pointer;
}

/* COMPUTER VISION */
.vision {
  background: #020617;
  color: #fff;
  text-align: center;
}

.vision-box {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-top: 40px;
}

.vision-box div {
  border: 1px solid #38bdf8;
  padding: 20px;
  border-radius: 10px;
}

/* LOGIN */
.login input {
  display: block;
  margin: 15px auto;
  padding: 12px;
  width: 300px;
}

.login button {
  display: block;
  margin: auto;
  padding: 12px 30px;
  background: #020617;
  color: #fff;
  border: none;
  cursor: pointer;
}

.note {
  text-align: center;
  margin-top: 10px;
  color: #666;
}

/* CART */
.cart {
  text-align: center;
}

.cart-item {
  display: flex;
  justify-content: space-between;
  max-width: 500px;
  margin: 10px auto;
}

.cart-item button {
  background: red;
  color: white;
  border: none;
  cursor: pointer;
  padding: 2px 6px;
}

/* FOOTER */
footer {
  background: #020617;
  color: #fff;
  padding: 25px;
  text-align: center;
}
</style>
</head>

<body>

<header class="navbar">
  <div class="logo">Rasa<span>Nusantara</span></div>
  <nav>
    <a href="#home">Halaman</a>
    <a href="#products">Menu</a>
    <a href="#vision">Tentang</a>
    <a href="#login">Login</a>
    <a href="#cart">🛒 <span id="cart-count">0</span></a>
  </nav>
</header>

<section id="home" class="hero">
  <h1>Cita Rasa Nusantara</h1>
  <p>Website e-commerce kuliner Indonesia Kelompok 2</p>
  <button onclick="scrollToShop()">Belanja Sekarang</button>
</section>

<section id="products">
<h2>Produk Unggulan</h2>

<div class="product-grid">

  <div class="product-card">
    <img src="https://i.pinimg.com/736x/7f/b8/d9/7fb8d98cb1943e743d15374e2174ee97.jpg">
    <h3>Ayam Betutu</h3>
    <p>Rp 65.000</p>
    <button onclick="addToCart('Ayam Betutu',65000)">Tambah</button>
  </div>

  <div class="product-card">
    <img src="https://i.pinimg.com/736x/eb/33/c7/eb33c7632c8e848308a4977e11fa3c18.jpg">
    <h3>Gorengan</h3>
    <p>Rp 40.000</p>
    <button onclick="addToCart('Gorengan',40000)">Tambah</button>
  </div>

  <div class="product-card">
    <img src="https://i.pinimg.com/736x/fc/ef/20/fcef207c38b18647b396d3ebe707819f.jpg">
    <h3>Mie Aceh</h3>
    <p>Rp 30.000</p>
    <button onclick="addToCart('Mie Aceh',30000)">Tambah</button>
  </div>

  <div class="product-card">
    <img src="https://i.pinimg.com/736x/65/99/d8/6599d8b5261f20d3f1863e94f6be9522.jpg">
    <h3>Gudeg</h3>
    <p>Rp 35.000</p>
    <button onclick="addToCart('Gudeg',35000)">Tambah</button>
  </div>

  <div class="product-card">
    <img src="https://i.pinimg.com/736x/f8/3d/7b/f83d7bb619e1a09958b4a97b40a186a6.jpg">
    <h3>Pempek</h3>
    <p>Rp 25.000</p>
    <button onclick="addToCart('Pempek',25000)">Tambah</button>
  </div>

  <div class="product-card">
    <img src="https://i.pinimg.com/736x/70/6c/ae/706cae701324ca56a2c4c5929f990574.jpg">
    <h3>Coto Makasar</h3>
    <p>Rp 25.000</p>
    <button onclick="addToCart('Coto Makasar',25000)">Tambah</button>
  </div>

  <div class="product-card">
    <img src="https://i.pinimg.com/1200x/3e/7e/d8/3e7ed8ccddc60a3bcc933c7839e5c025.jpg">
    <h3>Rawon</h3>
    <p>Rp 35.000</p>
    <button onclick="addToCart('Rawon',35000)">Tambah</button>
  </div>

  <div class="product-card">
    <img src="https://i.pinimg.com/736x/73/4f/d3/734fd391b64103b718e16b276a83b7f8.jpg">
    <h3>Rendang</h3>
    <p>Rp 50.000</p>
    <button onclick="addToCart('Rendang',50000)">Tambah</button>
  </div>

  <div class="product-card">
    <img src="https://i.pinimg.com/736x/81/70/66/817066a3e0587d60592d31920f31f69a.jpg">
    <h3>Sate</h3>
    <p>Rp 30.000</p>
    <button onclick="addToCart('Sate',30000)">Tambah</button>
  </div>

<div class="product-card">
    <img src="https://i.pinimg.com/1200x/7e/4d/51/7e4d512988f9e471e24eb8b1c2802e4c.jpg">
    <h3>Nasi Kuning Tumpeng</h3>
    <p>Rp 80.000</p>
    <button onclick="addToCart('Nasi Kuning Tumpeng',80000)">Tambah</button>
  </div>

<div class="product-card">
    <img src="https://i.pinimg.com/1200x/b7/33/d8/b733d8c9626b6543376295ce7ab075fd.jpg">
    <h3>Nasi Bakar</h3>
    <p>Rp 25.000</p>
    <button onclick="addToCart('Nasi Bakar',25000)">Tambah</button>
  </div>

<div class="product-card">
    <img src="https://i.pinimg.com/736x/3f/c6/a1/3fc6a129335adcbee534805ba8f2155f.jpg">
    <h3>Sate Lilit</h3>
    <p>Rp 35.000</p>
    <button onclick="addToCart('Sate Lilit',35000)">Tambah</button>
  </div>

</div>
</section>

<!-- COMPUTER VISION -->
<section id="vision" class="vision">
<h2>Rasa Nusantara</h2>
<p>
Website ini untuk mengenali produk makanan khas Nusantara Indonesia.
</p>

<div class="vision-box">
  <div>
    <h3>Web Developer</h3>
    <p>Niki Setiawan</p>
    
    <p>Novi Ramadhani</p><p>Lena Yulistia Ningsih</p>
  </div>
  <div>
    <h3>UI/UX & Konten</h3>
    
    
    <p>Suci Ramadhani</p><p> M.Daffa Pratama</p><p>Desy Fatmalia Putri</p><p>Sonia Karenina Br Purba</p>
    <p>Yesy AmandaSari Br Pasaribu</p>
   
  </div>
  <div>
    <h3>Dokumentasi</h3>
    
    <p>Dhanu Irfansyah</p>
    <p>Eki Restu Prianta</p><p>M.Dimas Nugraha </p><p>Azzura Althafalfarabi</p>
    <p>Rastra Hirarki Prawira</p>
    
  </div>
</div>
</section>

<!-- LOGIN -->
<section id="login" class="login">
<h2>Login Pengguna</h2>
<input type="text" placeholder="Username">
<input type="password" placeholder="Password">
<button onclick="login()">Login</button>
<p class="note">*Login simulasi (tanpa database)</p>
</section>


<section id="cart" class="cart">
<h2>Keranjang Belanja</h2>

<div id="cart-list"></div>

<p>Total item: <span id="cart-count-2">0</span></p>
<p><strong>Total harga: Rp <span id="total-price">0</span></strong></p>

<button onclick="checkout()">Checkout</button>
</section>

<footer>
<p>©️ 2026 Rasa Nusantara — Kelompok 2</p>
</footer>

<script>
let cart = [];

function addToCart(name, price) {
  let item = cart.find(p => p.name === name);
  if (item) item.qty++;
  else cart.push({ name, price, qty: 1 });
  updateCart();
}

function updateCart() {
  let list = document.getElementById("cart-list");
  let totalHarga = 0;
  let totalItem = 0;
  list.innerHTML = "";

  cart.forEach((item, i) => {
    totalHarga += item.price * item.qty;
    totalItem += item.qty;
    list.innerHTML += `
      <div class="cart-item">
        <span>${item.name} (${item.qty})</span>
        <span>Rp ${item.price * item.qty}
        <button onclick="removeItem(${i})">❌</button></span>
      </div>`;
  });

  document.getElementById("cart-count").innerText = totalItem;
  document.getElementById("cart-count-2").innerText = totalItem;
  document.getElementById("total-price").innerText = totalHarga;
}

function removeItem(i) {
  cart.splice(i, 1);
  updateCart();
}

function checkout() {
  alert("Checkout berhasil (simulasi)");
  cart = [];
  updateCart();
}

function login() {
  alert("Login berhasil (simulasi)");
}

function scrollToShop() {
  document.getElementById("products").scrollIntoView({behavior:"smooth"});
}
</script>

</body>
</html>
