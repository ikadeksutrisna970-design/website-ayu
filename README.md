<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ayu Pertiwi | Beauty & Lifestyle</title>

  <!-- Tailwind CSS & Google Fonts -->
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600;700&family=Quicksand:wght@500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: {
              bg: '#fcebf3',
              card: '#fff0f6',
              primary: '#ff7eb3',
              dark: '#e0528c',
              accent: '#ffb3c6',
              softYellow: '#fff9db'
            }
          },
          fontFamily: {
            fredoka: ['Fredoka', 'cursive', 'sans-serif'],
            quicksand: ['Quicksand', 'sans-serif']
          }
        }
      }
    }
  </script>

  <style>
    body {
      font-family: 'Quicksand', sans-serif;
      background-color: #fcebf3;
      background-image: radial-gradient(#ffa6c9 0.75px, transparent 0.75px);
      background-size: 16px 16px;
    }

    /* Animasi Pets (Kucing & Anjing) */
    @keyframes blink {
      0%, 90%, 100% { transform: scaleY(1); }
      95% { transform: scaleY(0.1); }
    }
    @keyframes wagCat {
      0%, 100% { transform: rotate(0deg); }
      50% { transform: rotate(18deg); }
    }
    @keyframes wagDog {
      0%, 100% { transform: rotate(-8deg); }
      50% { transform: rotate(22deg); }
    }

    .eye-anim { transform-origin: center; animation: blink 3.5s infinite; }
    .cat-tail-anim { transform-origin: bottom left; animation: wagCat 2s ease-in-out infinite; }
    .dog-tail-anim { transform-origin: bottom right; animation: wagDog 1.2s ease-in-out infinite; }
  </style>
</head>
<body class="text-gray-700 min-h-screen flex flex-col justify-between pb-10">

  <!-- NAVBAR -->
  <header class="sticky top-0 z-50 bg-white/90 backdrop-blur-md border-b-2 border-brand-accent/40 shadow-sm">
    <div class="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
      <div class="flex items-center gap-2 font-fredoka text-xl sm:text-2xl font-bold text-brand-dark">
        <span>🌸</span>
        <span>Ni Komang Ayu Pertiwi</span>
        <span class="text-xs bg-pink-100 text-brand-dark px-2 py-0.5 rounded-full border border-pink-300">♥</span>
      </div>

      <!-- Nav List -->
      <nav class="hidden md:flex items-center gap-6 text-sm font-semibold text-gray-600">
        <a href="#home" class="hover:text-brand-dark transition-colors">Home</a>
        <a href="#about" class="hover:text-brand-dark transition-colors">About Me</a>
        <a href="#shop" class="hover:text-brand-dark transition-colors">Shop</a>
        <a href="#portfolio" class="hover:text-brand-dark transition-colors">Portfolio</a>
        <a href="#contact" class="hover:text-brand-dark transition-colors">Contact</a>
      </nav>

      <button onclick="openModal()" class="bg-gradient-to-r from-pink-400 to-brand-primary text-white text-xs sm:text-sm font-bold px-4 py-2 rounded-full shadow-md hover:opacity-90 transition-all flex items-center gap-2">
        <i class="fa-solid fa-lock text-xs"></i>
        <span>Login Admin</span>
      </button>
    </div>
  </header>

  <!-- MAIN HERO SECTION -->
  <main class="max-w-6xl mx-auto px-4 mt-6 space-y-8" id="home">
    <div class="bg-white/80 rounded-3xl p-4 sm:p-8 border-4 border-white shadow-xl backdrop-blur-sm">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-center">
        
        <!-- KOLOM KIRI: Foto Profil & Quote -->
        <div class="lg:col-span-5 flex flex-col items-center text-center relative">
          <!-- Quote Badge Top -->
          <div class="bg-brand-softYellow border-2 border-amber-200 rounded-2xl p-3 shadow-sm mb-4 max-w-xs transform -rotate-1">
            <p class="font-fredoka text-xs text-amber-800">
              ✨ "A little progress each day leads to big results ♡"
            </p>
          </div>

          <!-- Foto Profil -->
          <div class="relative group">
            <div class="w-56 h-72 sm:w-64 sm:h-80 rounded-3xl overflow-hidden border-4 border-brand-accent shadow-lg bg-pink-100">
              <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=600&q=80" 
                   alt="Ayu Pertiwi" class="w-full h-full object-cover">
            </div>
            <!-- Decorative Tag -->
            <div class="absolute -bottom-3 bg-brand-dark text-white font-fredoka text-xs px-4 py-1.5 rounded-full shadow-md">
              Beauty & Lifestyle ✨
            </div>
          </div>
        </div>

        <!-- KOLOM KANAN: Detail Profil & Kontak Media Sosial -->
        <div class="lg:col-span-7 space-y-5">
          <!-- Judul Utama -->
          <div class="text-center lg:text-left">
            <h1 class="font-fredoka text-2xl sm:text-4xl text-brand-dark tracking-wide">
              Ni Komang Ayu Pertiwi Santa Yani
            </h1>
            <p class="text-xs sm:text-sm text-gray-500 font-medium mt-1">
              Store Specialist & Content Creator
            </p>
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
            <!-- Kartu About Me -->
            <div class="bg-brand-card p-4 rounded-2xl border border-pink-200 space-y-2" id="about">
              <div class="flex items-center gap-2 font-fredoka text-brand-dark text-sm border-b border-pink-200 pb-1">
                <i class="fa-solid fa-user-sparkles"></i>
                <span>About Me</span>
              </div>
              <ul class="text-xs space-y-1.5 text-gray-600 font-medium">
                <li>🎓 <b>Lulusan 2023</b> - Universitas Mataram</li>
                <li>📊 <b>S1</b> Ekonomi Pembangunan</li>
                <li>💼 <b>Bekerja di</b> PT SUPRA PRIMATAMA NUSANTARA (Biznet)</li>
                <li>🛍️ <b>Store Specialist</b> (2024 - sekarang)</li>
              </ul>
            </div>

            <!-- Kartu Dream Plan & Pets -->
            <div class="bg-white p-4 rounded-2xl border border-pink-200 flex flex-col justify-between items-center text-center">
              <div class="bg-pink-100 text-brand-dark rounded-2xl p-2 w-full border border-pink-300 font-fredoka text-xs">
                💖 Dream Plan ♡ Do Repeat ♡
              </div>

              <!-- ANIMASI KUCING & ANJING INTERAKTIF -->
              <div class="flex justify-center items-center gap-4 my-2">
                <!-- SVG Kucing -->
                <svg width="60" height="60" viewBox="0 0 100 100">
                  <path class="cat-tail-anim" d="M 30 75 Q 10 70 20 50" stroke="#ffb7b2" stroke-width="6" fill="none" stroke-linecap="round"/>
                  <ellipse cx="50" cy="70" rx="25" ry="20" fill="#ffdac1"/>
                  <circle cx="50" cy="45" r="22" fill="#ffdac1"/>
                  <polygon points="32,30 40,12 48,28" fill="#ffb7b2"/>
                  <polygon points="52,28 60,12 68,30" fill="#ffb7b2"/>
                  <ellipse class="eye-anim" cx="42" cy="42" rx="3" ry="4" fill="#4a4a4a"/>
                  <ellipse class="eye-anim" cx="58" cy="42" rx="3" ry="4" fill="#4a4a4a"/>
                  <circle cx="50" cy="48" r="2" fill="#ff80ab"/>
                </svg>

                <!-- SVG Anjing -->
                <svg width="60" height="60" viewBox="0 0 100 100">
                  <path class="dog-tail-anim" d="M 70 75 Q 90 65 80 50" stroke="#d4a373" stroke-width="6" fill="none" stroke-linecap="round"/>
                  <ellipse cx="50" cy="70" rx="25" ry="20" fill="#faedcd"/>
                  <circle cx="50" cy="45" r="22" fill="#faedcd"/>
                  <ellipse cx="28" cy="45" rx="6" ry="14" fill="#d4a373"/>
                  <ellipse cx="72" cy="45" rx="6" ry="14" fill="#d4a373"/>
                  <ellipse class="eye-anim" cx="42" cy="42" rx="3" ry="4" fill="#4a4a4a"/>
                  <ellipse class="eye-anim" cx="58" cy="42" rx="3" ry="4" fill="#4a4a4a"/>
                  <ellipse cx="50" cy="48" r="2.5" fill="#4a4a4a"/>
                </svg>
              </div>
            </div>
          </div>

          <!-- Tombol Kontak Media Sosial -->
          <div class="space-y-2 pt-2" id="contact">
            <p class="font-fredoka text-xs text-brand-dark text-center lg:text-left">Let's Connect ♡</p>
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-2 text-xs">
              <a href="https://wa.me/6287743969796" target="_blank" class="flex items-center justify-center gap-2 bg-green-500 text-white py-2 rounded-xl font-semibold shadow hover:bg-green-600 transition-colors">
                <i class="fa-brands fa-whatsapp text-sm"></i> WhatsApp
              </a>
              <a href="https://instagram.com/nmayu__" target="_blank" class="flex items-center justify-center gap-2 bg-pink-500 text-white py-2 rounded-xl font-semibold shadow hover:bg-pink-600 transition-colors">
                <i class="fa-brands fa-instagram text-sm"></i> Instagram
              </a>
              <a href="https://tiktok.com/@ayupertiwi89" target="_blank" class="flex items-center justify-center gap-2 bg-black text-white py-2 rounded-xl font-semibold shadow hover:bg-gray-800 transition-colors">
                <i class="fa-brands fa-tiktok text-sm"></i> TikTok
              </a>
              <a href="mailto:Nikomangayupertiwisantayani@gmail.com" class="flex items-center justify-center gap-2 bg-rose-400 text-white py-2 rounded-xl font-semibold shadow hover:bg-rose-500 transition-colors">
                <i class="fa-solid fa-envelope text-sm"></i> Email
              </a>
            </div>
          </div>

        </div>
      </div>
    </div>

    <!-- KATALOG PRODUK & AFFILIATE SECTION -->
    <section id="shop" class="space-y-4">
      <div class="flex items-center justify-between border-b-2 border-pink-200 pb-2">
        <h2 class="font-fredoka text-xl sm:text-2xl text-brand-dark flex items-center gap-2">
          <span>🛍️</span> Featured Products & Affiliate
        </h2>
        <span class="text-xs text-gray-500 font-semibold">Updated Automatically</span>
      </div>

      <!-- Grid Produk Responsive -->
      <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-4" id="productGrid">
        <!-- Render Javascript -->
      </div>
    </section>

    <!-- ADMIN DASHBOARD PANEL -->
    <section id="adminPanel" class="hidden bg-white p-6 rounded-3xl border-2 border-brand-dark shadow-lg">
      <h2 class="font-fredoka text-xl text-brand-dark mb-2">Dashboard Admin Ayu</h2>
      <p class="text-xs text-gray-500 mb-4">Tambah atau hapus produk rekomendasi affiliate kamu di sini:</p>

      <form id="addProductForm" class="grid grid-cols-1 sm:grid-cols-2 gap-3">
        <input type="text" id="pTitle" placeholder="Nama Produk" class="border border-pink-200 p-2.5 text-xs rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-primary" required>
        <input type="text" id="pCategory" placeholder="Kategori (cth: Skincare / Makeup)" class="border border-pink-200 p-2.5 text-xs rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-primary" required>
        <input type="text" id="pImg" placeholder="URL Foto Produk" class="border border-pink-200 p-2.5 text-xs rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-primary" required>
        <input type="text" id="pLink" placeholder="Link Affiliate Shopee/Tokopedia" class="border border-pink-200 p-2.5 text-xs rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-primary" required>
        
        <button type="submit" class="sm:col-span-2 bg-brand-primary text-white font-bold py-2.5 rounded-xl text-xs shadow hover:bg-brand-dark transition-colors">
          + Tambah Produk Ke Website
        </button>
      </form>

      <button onclick="logoutAdmin()" class="mt-4 text-xs text-gray-500 underline hover:text-red-500">
        Logout Admin
      </button>
    </section>
  </main>

  <!-- FOOTER -->
  <footer class="text-center text-xs text-pink-500 mt-10 font-medium">
    Thank you for visiting ♡ Keep shining! ✨ | © 2026 Ayu Pertiwi.
  </footer>

  <!-- MODAL LOGIN -->
  <div id="loginModal" class="fixed inset-0 bg-black/40 backdrop-blur-sm hidden items-center justify-center z-50 p-4">
    <div class="bg-white rounded-3xl p-6 w-full max-w-sm space-y-4 shadow-2xl border-2 border-pink-200">
      <h3 class="font-fredoka text-lg text-brand-dark text-center">Login Dashboard Admin</h3>
      <input type="password" id="adminPass" placeholder="Masukkan Password Admin" class="w-full border border-pink-200 p-3 rounded-xl text-xs focus:outline-none focus:ring-2 focus:ring-brand-primary">
      <button onclick="loginAdmin()" class="w-full bg-brand-primary text-white font-bold py-2.5 rounded-xl text-xs shadow hover:bg-brand-dark transition-all">
        Masuk
      </button>
      <button onclick="closeModal()" class="w-full text-xs text-gray-400 hover:text-gray-600 text-center block">
        Batal
      </button>
    </div>
  </div>

  <!-- JAVASCRIPT LOGIC -->
  <script>
    const defaultProducts = [
      {
        id: 1,
        title: "Skincare Set Glow Skin",
        category: "Skincare",
        img: "https://images.unsplash.com/photo-1556228720-195a672e8a03?auto=format&fit=crop&w=400&q=80",
        link: "https://shopee.co.id"
      },
      {
        id: 2,
        title: "Vintage Makeup Palette",
        category: "Makeup",
        img: "https://images.unsplash.com/photo-1512496015851-a90fb38ba796?auto=format&fit=crop&w=400&q=80",
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
        card.className = "bg-white rounded-2xl p-3 border border-pink-200 shadow-sm flex flex-col justify-between hover:shadow-md transition-shadow";
        card.innerHTML = `
          <div>
            <div class="h-36 rounded-xl overflow-hidden mb-2 bg-pink-50">
              <img src="${prod.img}" alt="${prod.title}" class="w-full h-full object-cover">
            </div>
            <span class="text-[10px] font-bold text-brand-dark bg-pink-100 px-2 py-0.5 rounded-full">${prod.category}</span>
            <h3 class="font-fredoka text-sm text-gray-800 mt-1 line-clamp-1">${prod.title}</h3>
          </div>
          <div class="mt-3">
            <a href="${prod.link}" target="_blank" class="block text-center bg-brand-primary text-white text-xs py-1.5 rounded-xl font-bold hover:bg-brand-dark transition-colors">
              Lihat Produk ➔
            </a>
            ${isAdmin ? `<button onclick="deleteProduct(${index})" class="w-full text-center text-[10px] text-red-500 mt-2 hover:underline">Hapus</button>` : ''}
          </div>
        `;
        grid.appendChild(card);
      });

      localStorage.setItem('ayu_products', JSON.stringify(products));
    }

    function openModal() { document.getElementById('loginModal').classList.remove('hidden'); document.getElementById('loginModal').classList.add('flex'); }
    function closeModal() { document.getElementById('loginModal').classList.add('hidden'); document.getElementById('loginModal').classList.remove('flex'); }

    function loginAdmin() {
      const pass = document.getElementById('adminPass').value;
      if (pass === "ayu123") {
        isAdmin = true;
        alert("Login Berhasil!");
        closeModal();
        document.getElementById('adminPanel').classList.remove('hidden');
        renderProducts();
      } else {
        alert("Password Salah!");
      }
    }

    function logoutAdmin() {
      isAdmin = false;
      document.getElementById('adminPanel').classList.add('hidden');
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
      if (confirm("Yakin ingin menghapus produk ini?")) {
        products.splice(index, 1);
        renderProducts();
      }
    }

    renderProducts();
  </script>
</body>
</html>
