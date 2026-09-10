<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ayu Pertiwi | Personal Portfolio & Shop</title>
  <style>
    /* --- CSS GLOBAL & THEME --- */
    :root {
      --bg-color: #fce4ec;
      --card-bg: #ffffff;
      --primary-pink: #ff80ab;
      --dark-pink: #c2185b;
      --text-color: #4a4a4a;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Poppins', cursive, sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      padding-bottom: 50px;
    }

    /* --- ANIMASI MATED KUCING & ANJING (SVG) --- */
    @keyframes blink {
      0%, 90%, 100% { transform: scaleY(1); }
      95% { transform: scaleY(0.1); }
    }

    @keyframes wag-tail {
      0%, 100% { transform: rotate(0deg); }
      50% { transform: rotate(15deg); }
    }

    @keyframes wag-tail-dog {
      0%, 100% { transform: rotate(-5deg); }
      50% { transform: rotate(20deg); }
    }

    .eye {
      transform-origin: center;
      animation: blink 4s infinite;
    }

    .cat-tail {
      transform-origin: bottom left;
      animation: wag-tail 2.5s ease-in-out infinite;
    }

    .dog-tail {
      transform-origin: bottom right;
      animation: wag-tail-dog 1.2s ease-in-out infinite;
    }

    .pets-container {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin: 20px 0;
    }

    /* --- NAVBAR --- */
    nav {
      background: white;
      padding: 15px 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.05);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    nav .logo {
      font-weight: bold;
      color: var(--dark-pink);
      font-size: 1.2rem;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 20px;
    }

    nav ul li a {
      text-decoration: none;
      color: var(--text-color);
      font-weight: 500;
    }

    .btn-login {
      background: var(--primary-pink);
      color: white;
      padding: 8px 16px;
      border-radius: 20px;
      border: none;
      cursor: pointer;
    }

    /* --- HERO SECTION --- */
    .hero {
      display: flex;
      flex-wrap: wrap;
      max-width: 1100px;
      margin: 30px auto;
      padding: 20px;
      background: #fff0f5;
      border-radius: 20px;
      border: 3px dashed var(--primary-pink);
      gap: 20px;
      align-items: center;
    }

    .hero-img {
      flex: 1;
      min-width: 280px;
      text-align: center;
    }

    .hero-img img {
      width: 100%;
      max-width: 350px;
      border-radius: 20px;
      border: 4px solid white;
    }

    .hero-bio {
      flex: 1;
      min-width: 280px;
    }

    .hero-bio h1 {
      color: var(--dark-pink);
      font-size: 2rem;
      margin-bottom: 10px;
    }

    .card-about {
      background: white;
      padding: 15px;
      border-radius: 15px;
      margin-top: 15px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    }

    /* --- PRODUCTS / AFFILIATE SECTION --- */
    .container {
      max-width: 1100px;
      margin: 40px auto;
      padding: 0 20px;
    }

    .section-title {
      text-align: center;
      color: var(--dark-pink);
      margin-bottom: 25px;
    }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    .product-card {
      background: white;
      border-radius: 15px;
      padding: 15px;
      text-align: center;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      border: 1px solid #f8bbd0;
      position: relative;
    }

    .product-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 10px;
    }

    .product-card h3 {
      margin: 10px 0 5px;
      color: var(--dark-pink);
    }

    .btn-affiliate {
      display: inline-block;
      margin-top: 10px;
      padding: 8px 15px;
      background-color: var(--primary-pink);
      color: white;
      text-decoration: none;
      border-radius: 15px;
      font-size: 0.9rem;
    }

    /* --- MODAL LOGIN & DASHBOARD ADMIN --- */
    .modal {
      display: none;
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0,0,0,0.5);
      justify-content: center;
      align-items: center;
      z-index: 200;
    }

    .modal-content {
      background: white;
      padding: 25px;
      border-radius: 15px;
      width: 90%;
      max-width: 400px;
    }

    .admin-panel {
      display: none;
      background: #fff;
      padding: 20px;
      border-radius: 15px;
      margin-top: 20px;
      border: 2px solid var(--dark-pink);
    }

    input {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .btn-delete {
      background: #e91e63;
      color: white;
      border: none;
      padding: 5px 10px;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 8px;
    }
  </style>
</head>
<body>

  <!-- NAVBAR -->
  <nav>
    <div class="logo">🌸 Ayu Pertiwi ♥</div>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#produk">Shop & Affiliate</a></li>
      <li><a href="#kontak">Contact</a></li>
    </ul>
    <button class="btn-login" onclick="openModal()">Login Admin</button>
  </nav>

  <!-- HERO / PROFILE SECTION -->
  <section class="hero">
    <div class="hero-img">
      <img src="https://via.placeholder.com/350x400/ffb6c1/ffffff?text=Foto+Ayu+Pertiwi" alt="Ayu Pertiwi">
    </div>
    <div class="hero-bio">
      <h1>Ni Komang Ayu Pertiwi</h1>
      <p><i>"A little progress each day leads to big results ♡"</i></p>

      <!-- ANIMATED PETS (KUCING & ANJING BERKEDIP & EKOR GERAK) -->
      <div class="pets-container">
        <!-- SVG Kucing -->
        <svg width="100" height="100" viewBox="0 0 100 100">
          <!-- Ekor Kucing -->
          <path class="cat-tail" d="M 30 75 Q 10 70 20 50" stroke="#ffb7b2" stroke-width="6" fill="none" stroke-linecap="round"/>
          <!-- Badan & Kepala Kucing -->
          <ellipse cx="50" cy="70" rx="25" ry="20" fill="#ffdac1"/>
          <circle cx="50" cy="45" r="22" fill="#ffdac1"/>
          <!-- Telinga Kucing -->
          <polygon points="32,30 40,12 48,28" fill="#ffb7b2"/>
          <polygon points="52,28 60,12 68,30" fill="#ffb7b2"/>
          <!-- Mata Kucing (Animasi Kedip) -->
          <ellipse class="eye" cx="42" cy="42" rx="3" ry="4" fill="#4a4a4a"/>
          <ellipse class="eye" cx="58" cy="42" rx="3" ry="4" fill="#4a4a4a"/>
          <!-- Hidung & Pipi -->
          <circle cx="50" cy="48" r="2" fill="#ff80ab"/>
          <ellipse cx="36" cy="48" rx="4" ry="2" fill="#ff9aa2" opacity="0.6"/>
          <ellipse cx="64" cy="48" rx="4" ry="2" fill="#ff9aa2" opacity="0.6"/>
        </svg>

        <!-- SVG Anjing -->
        <svg width="100" height="100" viewBox="0 0 100 100">
          <!-- Ekor Anjing -->
          <path class="dog-tail" d="M 70 75 Q 90 65 80 50" stroke="#d4a373" stroke-width="6" fill="none" stroke-linecap="round"/>
          <!-- Badan & Kepala Anjing -->
          <ellipse cx="50" cy="70" rx="25" ry="20" fill="#faedcd"/>
          <circle cx="50" cy="45" r="22" fill="#faedcd"/>
          <!-- Telinga Anjing (Jatuh) -->
          <ellipse cx="28" cy="45" rx="6" ry="14" fill="#d4a373"/>
          <ellipse cx="72" cy="45" rx="6" ry="14" fill="#d4a373"/>
          <!-- Mata Anjing (Animasi Kedip) -->
          <ellipse class="eye" cx="42" cy="42" rx="3" ry="4" fill="#4a4a4a"/>
          <ellipse class="eye" cx="58" cy="42" rx="3" ry="4" fill="#4a4a4a"/>
          <!-- Moncong & Hidung -->
          <ellipse cx="50" cy="50" rx="6" ry="4" fill="#fff"/>
          <ellipse cx="50" cy="48" r="2.5" fill="#4a4a4a"/>
          <ellipse cx="36" cy="48" rx="4" ry="2" fill="#ffb7b2" opacity="0.6"/>
          <ellipse cx="64" cy="48" rx="4" ry="2" fill="#ffb7b2" opacity="0.6"/>
        </svg>
      </div>

      <div class="card-about">
        <h3>About Me</h3>
        <ul>
          <li>🎓 Lulusan 2023 - Universitas Mataram</li>
          <li>📊 S1 Ekonomi Pembangunan</li>
          <li>💼 Store Specialist</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- PRODUK & AFFILIATE SECTION (PENGUNJUNG) -->
  <div class="container" id="produk">
    <h2 class="section-title">Featured Products & Recommendation</h2>
    <div class="product-grid" id="productGrid">
      <!-- Data produk akan dirender via JavaScript -->
    </div>
  </div>

  <!-- ADMIN PANEL (DASHBOARD AYU) -->
  <div class="container">
    <div class="admin-panel" id="adminPanel">
      <h2>Dashboard Admin Ayu</h2>
      <p>Kelola data produk & link affiliate di sini:</p>
      
      <form id="addProductForm" style="margin-top: 15px;">
        <input type="text" id="pTitle" placeholder="Nama Produk" required>
        <input type="text" id="pCategory" placeholder="Kategori (Misal: Skincare / Makeup)" required>
        <input type="text" id="pImg" placeholder="URL Foto Produk" required>
        <input type="text" id="pLink" placeholder="Link Affiliate Shopee/Tokopedia" required>
        <button type="submit" class="btn-login" style="width: 100%; margin-top: 10px;">+ Tambah Produk (Database)</button>
      </form>
      <button onclick="logoutAdmin()" style="margin-top: 15px; background: #666; color: white; border: none; padding: 8px 15px; border-radius: 8px;">Logout Admin</button>
    </div>
  </div>

  <!-- MODAL LOGIN -->
  <div class="modal" id="loginModal">
    <div class="modal-content">
      <h3 style="color: var(--dark-pink); margin-bottom: 10px;">Login Admin</h3>
      <input type="password" id="adminPass" placeholder="Masukkan Password Admin">
      <button class="btn-login" style="width: 100%; margin-top: 10px;" onclick="loginAdmin()">Login</button>
      <button onclick="closeModal()" style="width: 100%; margin-top: 5px; background: transparent; border: none; cursor: pointer;">Batal</button>
    </div>
  </div>

  <!-- JAVASCRIPT LOGIC (CRUD & STATE) -->
  <script>
    let defaultProducts = [
      {
        id: 1,
        title: "Skincare Set Glow",
        category: "Skincare",
        img: "https://via.placeholder.com/200/ffccd5/888888?text=Skincare",
        link: "https://shopee.co.id"
      },
      {
        id: 2,
        title: "Makeup Palette Vintage",
        category: "Makeup",
        img: "https://via.placeholder.com/200/ffccd5/888888?text=Makeup",
        link: "https://tokopedia.com"
      }
    ];

    let products = JSON.parse(localStorage.getItem('ayu_products')) || defaultProducts;
    let isAdmin = false;

    function renderProducts() {
      const grid = document.getElementById('productGrid');
      grid.innerHTML = '';

      products.forEach((prod, index) => {
        const card = document.createElement('div');
        card.className = 'product-card';
        card.innerHTML = `
          <img src="${prod.img}" alt="${prod.title}">
          <small style="color: #888;">${prod.category}</small>
          <h3>${prod.title}</h3>
          <a href="${prod.link}" target="_blank" class="btn-affiliate">Lihat Produk ➔</a>
          ${isAdmin ? `<br><button class="btn-delete" onclick="deleteProduct(${index})">Hapus</button>` : ''}
        `;
        grid.appendChild(card);
      });

      localStorage.setItem('ayu_products', JSON.stringify(products));
    }

    function openModal() { document.getElementById('loginModal').style.display = 'flex'; }
    function closeModal() { document.getElementById('loginModal').style.display = 'none'; }

    function loginAdmin() {
      const pass = document.getElementById('adminPass').value;
      if(pass === "ayu123") {
        isAdmin = true;
        alert("Login Berhasil!");
        closeModal();
        document.getElementById('adminPanel').style.display = 'block';
        renderProducts();
      } else {
        alert("Password Salah!");
      }
    }

    function logoutAdmin() {
      isAdmin = false;
      document.getElementById('adminPanel').style.display = 'none';
      renderProducts();
    }

    document.getElementById('addProductForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const newProd = {
        id: Date.now(),
        title: document.getElementById('pTitle').value,
        category: document.getElementById('pCategory').value,
        img: document.getElementById('pImg').value,
        link: document.getElementById('pLink').value
      };
      products.push(newProd);
      renderProducts();
      this.reset();
    });

    function deleteProduct(index) {
      if(confirm("Yakin ingin menghapus produk ini?")) {
        products.splice(index, 1);
        renderProducts();
      }
    }

    renderProducts();
  </script>
</body>
</html># website-ayu
