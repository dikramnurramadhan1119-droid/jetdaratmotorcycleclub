<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JDMC - Jet Darat Motorcycle Club | Satu Mimpi Roleplay</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #0f0f0f;
            --bg-card: #1a1a1a;
            --primary: #f39c12; /* Warna khas motor/gahar */
            --text-main: #ffffff;
            --text-muted: #b0b0b0;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
        }

        /* Header & Navigasi */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(15, 15, 15, 0.95);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            z-index: 1000;
            border-bottom: 2px solid rgba(243, 156, 18, 0.2);
        }

        .logo-brand {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-brand img {
            width: 45px;
            height: 45px;
            object-fit: contain;
        }

        .logo-brand h1 {
            font-size: 1.2rem;
            font-weight: 700;
            letter-spacing: 1px;
            color: var(--primary);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--text-main);
            font-weight: 600;
            transition: var(--transition);
        }

        nav ul li a:hover {
            color: var(--primary);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.85)), url('https://images.unsplash.com/photo-1558981403-c5f9899a28bc?auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
        }

        .hero img.main-logo {
            width: 150px;
            height: 150px;
            margin-bottom: 20px;
            filter: drop-shadow(0 0 15px rgba(243, 156, 18, 0.6));
        }

        .hero h2 {
            font-size: 2.8rem;
            font-weight: 800;
            text-transform: uppercase;
            margin-bottom: 10px;
            color: var(--text-main);
        }

        .hero h2 span {
            color: var(--primary);
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--text-muted);
            max-width: 600px;
            margin-bottom: 30px;
        }

        .btn {
            background-color: var(--primary);
            color: var(--bg-dark);
            padding: 12px 30px;
            border-radius: 5px;
            font-weight: 700;
            text-decoration: none;
            transition: var(--transition);
        }

        .btn:hover {
            background-color: #d35400;
            color: var(--text-main);
            transform: translateY(-3px);
        }

        /* General Section Styling */
        section {
            padding: 100px 50px 80px 50px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h3 {
            font-size: 2.2rem;
            font-weight: 700;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .section-title h3 span {
            color: var(--primary);
        }

        .section-title p {
            color: var(--text-muted);
        }

        /* Asal Usul Section */
        .history-content {
            background: var(--bg-card);
            padding: 40px;
            border-radius: 10px;
            border-left: 5px solid var(--primary);
        }

        .history-content p {
            margin-bottom: 20px;
            color: var(--text-muted);
            text-align: justify;
        }

        /* Album & Media Section */
        .media-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .media-card {
            background: var(--bg-card);
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid rgba(255,255,255,0.05);
            transition: var(--transition);
        }

        .media-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
        }

        .media-card img, .media-card iframe {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border: none;
        }

        .media-card .card-body {
            padding: 20px;
        }

        .media-card h4 {
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .media-card p {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* Struktur Jabatan Section */
        .structure-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .structure-card {
            background: var(--bg-card);
            text-align: center;
            padding: 30px 20px;
            border-radius: 8px;
            border-bottom: 4px solid var(--primary);
            transition: var(--transition);
        }

        .structure-card:hover {
            transform: translateY(-5px);
            background: #222;
        }

        .structure-card h4 {
            color: var(--primary);
            font-size: 1.2rem;
            margin-bottom: 5px;
            text-transform: uppercase;
        }

        .structure-card h5 {
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .structure-card p {
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        /* Footer */
        footer {
            background: #0a0a0a;
            text-align: center;
            padding: 30px;
            color: var(--text-muted);
            border-top: 1px solid rgba(255,255,255,0.05);
            font-size: 0.9rem;
        }

        /* Responsive Mobile */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero * {
            animation: fadeIn 1s ease-in-out;
        }
    </style>
</head>
<body>

    <!-- Header & Navigasi -->
    <header>
        <div class="logo-brand">
            <!-- Ganti src dengan link logo Anda -->
            <img src="https://cdn-icons-png.flaticon.com/512/3241/3241113.png" alt="Logo JDMC">
            <h1>JDMC - SATU MIMPI</h1>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#asal-usul">Asal Usul</a></li>
                <li><a href="#album">Album & Media</a></li>
                <li><a href="#struktur">Struktur</a></li>
            </ul>
        </nav>
    </header>

    <!-- Halaman Utama / Hero Section -->
    <section id="home" class="hero">
        <!-- Ganti src dengan link logo utama Anda -->
        <img src="https://cdn-icons-png.flaticon.com/512/3241/3241113.png" alt="Logo JDMC Besar" class="main-logo">
        <h2>Jet Darat <span>Motorcycle Club</span></h2>
        <p>Solidaritas Tanpa Batas di Atas Aspal. Klub motor resmi penguasa jalanan kota Satu Mimpi Roleplay.</p>
        <a href="#asal-usul" class="btn">Jelajahi Klub</a>
    </section>

    <!-- Asal Usul JDMC -->
    <section id="asal-usul">
        <div class="section-title">
            <h3>Asal Usul <span>JDMC</span></h3>
            <p>Sejarah dan filosofi berdirinya klub di Satu Mimpi Roleplay</p>
        </div>
        <div class="history-content">
            <p><strong>Jet Darat Motorcycle Club (JDMC)</strong> lahir dari perkumpulan para pencinta kecepatan dan loyalitas tinggi di jalanan kota Satu Mimpi Roleplay. Bermula dari sekelompok pengendara motor independen yang sering berkumpul di sudut kota, mereka memutuskan untuk menyatukan visi dan membentuk sebuah keluarga besar berbasis brotherhood.</p>
            <p>Nama "Jet Darat" dipilih untuk merepresentasikan kecepatan, ketangguhan mesin, serta ketepatan dalam mengambil keputusan di atas aspal jalanan kota. Bagi member JDMC, motor bukan sekadar alat transportasi, melainkan simbol kebebasan dan harga diri.</p>
            <p>Hingga kini, JDMC terus memegang teguh prinsip solidaritas tanpa batas, menghormati sesama klub, dan menjaga ketertiban serta keseruan dalam ekosistem roleplay di Satu Mimpi.</p>
        </div>
    </section>

    <!-- Album & Media (YouTube & TikTok) -->
    <section id="album">
        <div class="section-title">
            <h3>Album & <span>Media Member</span></h3>
            <p>Dokumentasi aktivitas in-game dan kreasi video member JDMC</p>
        </div>
        <div class="media-grid">
            <!-- Contoh Card Album Foto -->
            <div class="media-card">
                <img src="https://images.unsplash.com/photo-1568772585407-9361f9bf3a87?auto=format&fit=crop&w=600&q=80" alt="Touring Malam">
                <div class="card-body">
                    <h4>Night Ride City Tour</h4>
                    <p>Kumpul bareng keliling kota Satu Mimpi Roleplay menikmati malam.</p>
                </div>
            </div>
            <!-- Contoh Card Embed YouTube -->
            <div class="media-card">
                <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="YouTube video player" allowfullscreen></iframe>
                <div class="card-body">
                    <h4>Cinematic Ride JDMC</h4>
                    <p>By: @MemberJDMC - Aksi kebersamaan member di jalan raya.</p>
                </div>
            </div>
            <!-- Contoh Card TikTok Link -->
            <div class="media-card">
                <img src="https://images.unsplash.com/photo-1558980664-3a031cf67ea8?auto=format&fit=crop&w=600&q=80" alt="TikTok Content">
                <div class="card-body">
                    <h4>TikTok Showcase</h4>
                    <p>Kumpulan momen kocak dan roleplay seru member di TikTok.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Struktur Jabatan Klub -->
    <section id="struktur">
        <div class="section-title">
            <h3>Struktur <span>Organisasi</span></h3>
            <p>Hierarki kepengurusan Jet Darat Motorcycle Club</p>
        </div>
        <div class="structure-grid">
            <div class="structure-card">
                <h4>President / Founder</h4>
                <h5>[Nama IC / Karakter]</h5>
                <p>Pemimpin tertinggi pengambil kebijakan klub.</p>
            </div>
            <div class="structure-card">
                <h4>Vice President</h4>
                <h5>[Nama IC / Karakter]</h5>
                <p>Wakil pemimpin dan pengawas operasional harian.</p>
            </div>
            <div class="structure-card">
                <h4>Road Captain</h4>
                <h5>[Nama IC / Karakter]</h5>
                <p>Pemimpin formasi dan rute saat touring/konvoi.</p>
            </div>
            <div class="structure-card">
                <h4>Treasurer</h4>
                <h5>[Nama IC / Karakter]</h5>
                <p>Pengelola keuangan dan logistik kas klub.</p>
            </div>
            <div class="structure-card">
                <h4>Enforcer</h4>
                <h5>[Nama IC / Karakter]</h5>
                <p>Keamanan internal dan pelindung nama baik klub.</p>
            </div>
            <div class="structure-card">
                <h4>Full Member / Prospek</h4>
                <h5>[Daftar Anggota Aktif]</h5>
                <p>Keluarga inti dan calon anggota resmi JDMC.</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Jet Darat Motorcycle Club (JDMC) - Server Satu Mimpi Roleplay. All Rights Reserved.</p>
    </footer>

</body>
</html>
