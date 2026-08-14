  <!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#080808">

<title>JDMC | Jet Darat Motorcycle Club</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;600;700&family=Poppins:wght@300;400;500;600;700;800&display=swap');

:root{
  --black:#050505;
  --dark:#0b0b0b;
  --card:#111111;
  --card2:#171717;
  --line:#292929;
  --gold:#f5a623;
  --gold2:#ffca57;
  --white:#ffffff;
  --gray:#999999;
  --red:#d71920;
}

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

html{
  scroll-behavior:smooth;
}

body{
  background:var(--black);
  color:var(--white);
  font-family:Poppins,Arial,sans-serif;
  overflow-x:hidden;
}

/* =========================
   LOADING
========================= */

#loader{
  position:fixed;
  inset:0;
  z-index:99999;
  background:#030303;
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;
  transition:.6s ease;
}

#loader.hide{
  opacity:0;
  visibility:hidden;
}

.loader-logo{
  width:125px;
  height:125px;
  object-fit:contain;
  animation:loaderPulse 1.5s infinite;
}

.loader-title{
  margin-top:18px;
  font-family:Oswald,sans-serif;
  font-size:28px;
  letter-spacing:7px;
  color:var(--gold);
}

.loader-bar{
  width:190px;
  height:3px;
  margin-top:18px;
  background:#222;
  overflow:hidden;
}

.loader-bar span{
  display:block;
  width:50%;
  height:100%;
  background:var(--gold);
  animation:loaderMove 1.2s infinite;
}

@keyframes loaderPulse{
  50%{transform:scale(1.08)}
}

@keyframes loaderMove{
  from{transform:translateX(-120%)}
  to{transform:translateX(320%)}
}

/* =========================
   HEADER
========================= */

header{
  position:fixed;
  top:0;
  left:0;
  width:100%;
  z-index:5000;
  background:rgba(5,5,5,.94);
  backdrop-filter:blur(12px);
  border-bottom:1px solid rgba(245,166,35,.25);
}

.nav{
  max-width:1250px;
  margin:auto;
  min-height:72px;
  padding:10px 22px;
  display:flex;
  align-items:center;
  justify-content:space-between;
}

.logo-wrap{
  display:flex;
  align-items:center;
  gap:12px;
  text-decoration:none;
  color:white;
}

.logo-wrap img{
  width:48px;
  height:48px;
  object-fit:contain;
}

.logo-text{
  font-family:Oswald,sans-serif;
  font-size:20px;
  letter-spacing:1px;
}

.logo-text span{
  color:var(--gold);
}

nav{
  display:flex;
  gap:24px;
}

nav a{
  color:#ddd;
  text-decoration:none;
  font-size:13px;
  font-weight:700;
  transition:.25s;
}

nav a:hover{
  color:var(--gold);
}

/* =========================
   HERO
========================= */

.hero{
  min-height:100vh;
  position:relative;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  padding:120px 20px 70px;
  background:
    linear-gradient(180deg,rgba(0,0,0,.55),rgba(0,0,0,.94)),
    url("images/sampul-jdmc.jpg") center/cover no-repeat;
}

.hero:after{
  content:"";
  position:absolute;
  inset:0;
  background:radial-gradient(circle at center,transparent 15%,rgba(0,0,0,.7) 100%);
  pointer-events:none;
}

.hero-content{
  position:relative;
  z-index:2;
  max-width:950px;
}

.hero-logo{
  width:180px;
  height:180px;
  object-fit:contain;
  filter:drop-shadow(0 0 30px rgba(245,166,35,.35));
}

.hero h1{
  margin-top:18px;
  font-family:Oswald,sans-serif;
  font-size:clamp(48px,8vw,90px);
  line-height:.92;
  text-transform:uppercase;
}

.hero h1 span{
  color:var(--gold);
}

.hero p{
  max-width:700px;
  margin:25px auto;
  color:#c8c8c8;
  line-height:1.8;
  font-size:15px;
}

.hero-buttons{
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:12px;
}

.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  min-width:150px;
  padding:13px 22px;
  border-radius:5px;
  text-decoration:none;
  font-size:13px;
  font-weight:800;
  transition:.25s;
}

.btn-gold{
  background:var(--gold);
  color:#080808;
}

.btn-gold:hover{
  background:var(--gold2);
  transform:translateY(-3px);
}

.btn-outline{
  border:1px solid #555;
  color:white;
  background:rgba(0,0,0,.35);
}

.btn-outline:hover{
  border-color:var(--gold);
  color:var(--gold);
}

/* =========================
   SECTIONS
========================= */

section{
  max-width:1250px;
  margin:auto;
  padding:90px 22px;
}

.heading{
  text-align:center;
  margin-bottom:42px;
}

.heading small{
  color:var(--gold);
  font-size:11px;
  font-weight:800;
  letter-spacing:4px;
}

.heading h2{
  margin:8px 0;
  font-family:Oswald,sans-serif;
  font-size:42px;
  text-transform:uppercase;
}

.heading h2 span{
  color:var(--gold);
}

.heading p{
  color:var(--gray);
  font-size:13px;
}

/* =========================
   ABOUT
========================= */

.about{
  background:linear-gradient(145deg,#151515,#0b0b0b);
  border:1px solid var(--line);
  border-left:4px solid var(--gold);
  border-radius:8px;
  padding:35px;
}

.about p{
  color:#c5c5c5;
  line-height:1.9;
  margin-bottom:14px;
}

.about p:last-child{
  margin-bottom:0;
}

.stats{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:15px;
  margin-top:18px;
}

.stat{
  background:var(--card);
  border:1px solid var(--line);
  padding:22px 10px;
  text-align:center;
}

.stat strong{
  display:block;
  font-family:Oswald,sans-serif;
  color:var(--gold);
  font-size:35px;
}

.stat span{
  color:#888;
  font-size:10px;
  text-transform:uppercase;
}

/* =========================
   MEMBER TOOLS
========================= */

.search{
  width:100%;
  padding:15px 17px;
  border:1px solid #333;
  border-radius:5px;
  background:#101010;
  color:white;
  outline:none;
  font-family:Poppins,sans-serif;
  margin-bottom:15px;
}

.search:focus{
  border-color:var(--gold);
}

.filters{
  display:flex;
  flex-wrap:wrap;
  gap:7px;
}

.filter{
  border:1px solid #333;
  background:#121212;
  color:#bbb;
  padding:8px 12px;
  border-radius:4px;
  cursor:pointer;
  font-family:Poppins,sans-serif;
  font-size:10px;
  font-weight:800;
  transition:.2s;
}

.filter:hover,
.filter.active{
  background:var(--gold);
  color:#000;
  border-color:var(--gold);
}

/* =========================
   RANK
========================= */

.rank{
  margin-top:50px;
}

.rank:first-child{
  margin-top:0;
}

.rank-header{
  display:flex;
  align-items:center;
  gap:12px;
  margin-bottom:18px;
  padding-bottom:11px;
  border-bottom:1px solid var(--line);
}

.rank-number{
  width:39px;
  height:39px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:var(--gold);
  color:#000;
  border-radius:4px;
  font-weight:900;
}

.rank-header h3{
  font-family:Oswald,sans-serif;
  font-size:26px;
  letter-spacing:1px;
}

/* =========================
   MEMBER CARDS
========================= */

.member-grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(225px,1fr));
  gap:18px;
}

.member-card{
  position:relative;
  background:linear-gradient(145deg,#171717,#0d0d0d);
  border:1px solid #292929;
  border-radius:7px;
  overflow:hidden;
  transition:.3s;
}

.member-card:hover{
  transform:translateY(-6px);
  border-color:var(--gold);
  box-shadow:0 15px 35px rgba(0,0,0,.45);
}

.member-photo{
  width:100%;
  height:290px;
  display:block;
  object-fit:cover;
  background:#111;
}

.member-content{
  padding:16px;
}

.member-name{
  font-size:16px;
  font-weight:700;
  line-height:1.35;
}

.member-role{
  display:inline-block;
  margin-top:5px;
  color:var(--gold);
  font-size:9px;
  font-weight:800;
  letter-spacing:1px;
  text-transform:uppercase;
}

.socials{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:7px;
  margin-top:14px;
}

.social{
  padding:9px 5px;
  text-align:center;
  text-decoration:none;
  border-radius:4px;
  color:white;
  font-size:10px;
  font-weight:800;
  transition:.2s;
}

.social:hover{
  transform:translateY(-2px);
  opacity:.85;
}

.yt{
  background:#d90000;
}

.tt{
  background:#080808;
  border:1px solid #444;
}

.unavailable{
  grid-column:1 / -1;
  text-align:center;
  border:1px dashed #333;
  padding:8px;
  color:#777;
  font-size:10px;
}

/* =========================
   MEDIA
========================= */

.media-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:20px;
}

.media-card{
  background:#111;
  border:1px solid var(--line);
  border-radius:7px;
  overflow:hidden;
}

.media-card video{
  width:100%;
  height:300px;
  display:block;
  background:#000;
  object-fit:cover;
}

.media-card img{
  width:100%;
  height:300px;
  display:block;
  object-fit:cover;
}

.media-info{
  padding:18px;
}

.media-info h3{
  font-family:Oswald,sans-serif;
  font-size:23px;
}

.media-info p{
  margin-top:5px;
  color:#888;
  font-size:12px;
}

/* =========================
   ANTHEM
========================= */

.anthem{
  background:
    linear-gradient(rgba(0,0,0,.72),rgba(0,0,0,.9)),
    url("images/sampul-jdmc.jpg") center/cover;
  border:1px solid #333;
  border-radius:8px;
  text-align:center;
  padding:45px 20px;
}

.anthem img{
  width:100px;
  height:100px;
  object-fit:contain;
}

.anthem h3{
  font-family:Oswald,sans-serif;
  font-size:32px;
  margin:12px 0 4px;
}

.anthem p{
  color:#999;
  margin-bottom:20px;
  font-size:13px;
}

audio{
  width:min(600px,100%);
}

/* =========================
   FOOTER
========================= */

footer{
  border-top:1px solid #222;
  background:#030303;
  text-align:center;
  padding:35px 20px;
}

footer img{
  width:65px;
  height:65px;
  object-fit:contain;
}

footer h3{
  margin:10px 0 5px;
  font-family:Oswald,sans-serif;
  color:var(--gold);
}

footer p{
  color:#666;
  font-size:11px;
}

/* =========================
   MOBILE
========================= */

@media(max-width:800px){

  .nav{
    min-height:60px;
    padding:8px 14px;
  }

  .logo-wrap img{
    width:40px;
    height:40px;
  }

  .logo-text{
    font-size:15px;
  }

  nav{
    display:none;
  }

  section{
    padding:70px 14px;
  }

  .hero{
    padding-top:100px;
  }

  .hero-logo{
    width:145px;
    height:145px;
  }

  .hero h1{
    font-size:48px;
  }

  .hero p{
    font-size:12px;
  }

  .heading h2{
    font-size:32px;
  }

  .about{
    padding:24px;
  }

  .stats{
    grid-template-columns:repeat(2,1fr);
  }

  .member-grid{
    grid-template-columns:repeat(2,1fr);
    gap:9px;
  }

  .member-photo{
    height:215px;
  }

  .member-content{
    padding:11px;
  }

  .member-name{
    font-size:12px;
  }

  .member-role{
    font-size:8px;
  }

  .social{
    font-size:8px;
    padding:8px 3px;
  }

  .media-grid{
    grid-template-columns:1fr;
  }

  .media-card video,
  .media-card img{
    height:240px;
  }
}

@media(max-width:390px){

  .member-photo{
    height:190px;
  }

  .member-name{
    font-size:11px;
  }

  .hero h1{
    font-size:42px;
  }
}
</style>
</head>

<body>

<!-- =========================
     LOADING
========================= -->

<div id="loader">
  <img src="images/logo-jdmc.png" class="loader-logo" alt="JDMC">
  <div class="loader-title">JDMC</div>
  <div class="loader-bar"><span></span></div>
</div>


<!-- =========================
     HEADER
========================= -->

<header>
  <div class="nav">

    <a href="#home" class="logo-wrap">
      <img src="images/logo-jdmc.png" alt="JDMC">
      <div class="logo-text">
        JDMC <span>•</span> MOTORCYCLE CLUB
      </div>
    </a>

    <nav>
      <a href="#home">HOME</a>
      <a href="#about">ABOUT</a>
      <a href="#members">MEMBERS</a>
      <a href="#media">MEDIA</a>
      <a href="#anthem">ANTHEM</a>
    </nav>

  </div>
</header>


<!-- =========================
     HERO
========================= -->

<section class="hero" id="home">

  <div class="hero-content">

    <img
      src="images/logo-jdmc.png"
      class="hero-logo"
      alt="JDMC Logo"
    >

    <h1>
      JET DARAT<br>
      <span>MOTORCYCLE CLUB</span>
    </h1>

    <p>
      Brotherhood • Loyalty • Respect<br>
      Official JDMC Member Directory
    </p>

    <div class="hero-buttons">
      <a href="#members" class="btn btn-gold">
        LIHAT MEMBER
      </a>

      <a href="#anthem" class="btn btn-outline">
        JDMC ANTHEM
      </a>
    </div>

  </div>

</section>


<!-- =========================
     ABOUT
========================= -->

<section id="about">

  <div class="heading">
    <small>WHO WE ARE</small>
    <h2>ABOUT <span>JDMC</span></h2>
    <p>Jet Darat Motorcycle Club</p>
  </div>

  <div class="about">

    <p>
      <strong>Jet Darat Motorcycle Club (JDMC)</strong>
      adalah motorcycle club dalam dunia
      <strong>Satu Mimpi Roleplay.</strong>
    </p>

    <p>
      Website ini menjadi pusat informasi keluarga JDMC,
      berisi struktur jabatan, profil member, serta link
      YouTube dan TikTok masing-masing anggota.
    </p>

    <p>
      Satu klub. Satu keluarga. Satu mimpi.
    </p>

  </div>

  <div class="stats">

    <div class="stat">
      <strong>26</strong>
      <span>Member</span>
    </div>

    <div class="stat">
      <strong>9</strong>
      <span>Jabatan</span>
    </div>

    <div class="stat">
      <strong>25</strong>
      <span>YouTube</span>
    </div>

    <div class="stat">
      <strong>26</strong>
      <span>TikTok</span>
    </div>

  </div>

</section>


<!-- =========================
     MEMBERS
========================= -->

<section id="members">

  <div class="heading">
    <small>THE BROTHERHOOD</small>
    <h2>JDMC <span>MEMBERS</span></h2>
    <p>26 anggota • 9 jabatan</p>
  </div>

  <input
    type="search"
    id="search"
    class="search"
    placeholder="🔎 Cari nama member atau jabatan..."
  >

  <div class="filters">

    <button class="filter active" data-filter="all">SEMUA</button>
    <button class="filter" data-filter="Charter Veteran">CHARTER VETERAN</button>
    <button class="filter" data-filter="President">PRESIDENT</button>
    <button class="filter" data-filter="Vice President">VICE PRESIDENT</button>
    <button class="filter" data-filter="Sergeant at Arms">SERGEANT AT ARMS</button>
    <button class="filter" data-filter="Road Captain">ROAD CAPTAIN</button>
    <button class="filter" data-filter="Secretary">SECRETARY</button>
    <button class="filter" data-filter="Enforcer">ENFORCER</button>
    <button class="filter" data-filter="Member">MEMBER</button>
    <button class="filter" data-filter="Prospect">PROSPECT</button>

  </div>

  <div id="members-container"></div>

</section>


<!-- =========================
     MEDIA
========================= -->

<section id="media">

  <div class="heading">
    <small>JDMC ARCHIVE</small>
    <h2>JDMC <span>MEDIA</span></h2>
    <p>Dokumentasi Jet Darat Motorcycle Club</p>
  </div>

  <div class="media-grid">

    <div class="media-card">

      <img
        src="images/sampul-jdmc.jpg"
        alt="JDMC"
      >

      <div class="media-info">
        <h3>JDMC Brotherhood</h3>
        <p>
          Official JDMC media archive.
        </p>
      </div>

    </div>

    <div class="media-card">

      <video controls playsinline preload="metadata">
        <source
          src="video/jdmc-video.mp4"
          type="video/mp4"
        >
        Video tidak dapat diputar di browser ini.
      </video>

      <div class="media-info">
        <h3>JDMC Video</h3>
        <p>
          Dokumentasi video JDMC.
        </p>
      </div>

    </div>

  </div>

</section>


<!-- =========================
     ANTHEM
========================= -->

<section id="anthem">

  <div class="heading">
    <small>JDMC SOUND</small>
    <h2>JDMC <span>ANTHEM</span></h2>
    <p>Official JDMC soundtrack</p>
  </div>

  <div class="anthem">

    <img
      src="images/logo-jdmc.png"
      alt="JDMC Logo"
    >

    <h3>JDMC ANTHEM</h3>

    <p>
      Jet Darat Motorcycle Club
    </p>

    <audio controls preload="metadata">
      <source
        src="music/jdmc-anthem.mp3"
        type="audio/mpeg"
      >
      Browser kamu tidak mendukung audio.
    </audio>

  </div>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

  <img
    src="images/logo-jdmc.png"
    alt="JDMC"
  >

  <h3>JET DARAT MOTORCYCLE CLUB</h3>

  <p>JDMC • Satu Mimpi Roleplay</p>

  <p style="margin-top:7px;">
    © 2026 JDMC
  </p>

</footer>


<script>

/* =====================================================
   JDMC MASTER DATA
   DATA TERAKHIR YANG KAMU BERIKAN
===================================================== */

const members = [

  {
    name:"Crystal Oda M. Cougan",
    role:"Charter Veteran",
    photo:"crystal-oda.jpg",
    youtube:"https://youtube.com/@ic.crystal",
    tiktok:"https://www.tiktok.com/@mrs.jocrys"
  },

  {
    name:"Joko Sancez",
    role:"Charter Veteran",
    photo:"joko-sancez.jpg",
    youtube:"https://youtube.com/@luckystrikegaming",
    tiktok:"https://www.tiktok.com/@jsluckystrike"
  },

  {
    name:"Gashima",
    role:"President",
    photo:"gashima.jpg",
    youtube:"https://youtube.com/@ananggaming",
    tiktok:"https://www.tiktok.com/@anangwaw"
  },

  {
    name:"Melody",
    role:"Vice President",
    photo:"melody.jpg",
    youtube:"https://youtube.com/@queenuts",
    tiktok:"https://www.tiktok.com/@queeenuts"
  },

  {
    name:"Troy",
    role:"Sergeant at Arms",
    photo:"troy.jpg",
    youtube:"https://youtube.com/@truega9",
    tiktok:"https://www.tiktok.com/@troypon"
  },

  {
    name:"Gonzales",
    role:"Sergeant at Arms",
    photo:"gonzales.jpg",
    youtube:"https://youtube.com/@reynoyabrirenel",
    tiktok:"https://www.tiktok.com/@rembel69"
  },

  {
    name:"Otyy Parker",
    role:"Road Captain",
    photo:"otyy-parker.jpg",
    youtube:"https://youtube.com/@otyyybby",
    tiktok:"https://www.tiktok.com/@otyybby"
  },

  {
    name:"Rexy Jaegerjaquez",
    role:"Road Captain",
    photo:"rexy-jaegerjaquez.jpg",
    youtube:"https://youtube.com/@CallMeRexyz",
    tiktok:"https://www.tiktok.com/@callmerexyz"
  },

  {
    name:"Bianca Cosanostra",
    role:"Secretary",
    photo:"bianca-cosanostra.jpg",
    youtube:"https://youtube.com/@Bloodyy_Queen",
    tiktok:"https://www.tiktok.com/@c.monroe"
  },

  {
    name:"Senandungchu Darmawan",
    role:"Secretary",
    photo:"senandungchu-darmawan.jpg",
    youtube:"https://youtube.com/@NoyaLacune",
    tiktok:"https://www.tiktok.com/@noyslacune"
  },

  {
    name:"Jay Jo",
    role:"Enforcer",
    photo:"jay-jo.jpg",
    youtube:"https://youtube.com/@jaymfjo",
    tiktok:"https://www.tiktok.com/@jaymfjo"
  },

  {
    name:"Ilona K. De Fontaine",
    role:"Member",
    photo:"ilona-k-de-fontaine.jpg",
    youtube:"https://youtube.com/@ilonaclementine",
    tiktok:"https://www.tiktok.com/@ilonaclementine"
  },

  {
    name:"Nekomata W Rosevale",
    role:"Member",
    photo:"nekomata-w-rosevale.jpg",
    youtube:"https://youtube.com/@kazemiyaneko",
    tiktok:"https://www.tiktok.com/@nekoyamarawr"
  },

  {
    name:"Philip W Inagawa",
    role:"Member",
    photo:"philip-w-inagawa.jpg",
    youtube:"https://youtube.com/@Philip.lampuu",
    tiktok:"https://www.tiktok.com/@philip.lampuu"
  },

  {
    name:"Tannya Isla Judith",
    role:"Member",
    photo:"tannya-isla-judith.jpg",
    youtube:"https://youtube.com/@Flourllie",
    tiktok:"https://www.tiktok.com/@internethateu"
  },

  {
    name:"Rickie Moreau",
    role:"Member",
    photo:"rickie-moreau.jpg",
    youtube:"https://youtube.com/@moreau__1",
    tiktok:"https://www.tiktok.com/@rickkiecsr"
  },

  {
    name:"James Matthew G",
    role:"Member",
    photo:"james-matthew-g.jpg",
    youtube:"https://youtube.com/@JamesMatthewG",
    tiktok:"https://www.tiktok.com/@matthew.garcia14"
  },

  {
    name:"Aceng Resing",
    role:"Member",
    photo:"aceng-resing.jpg",
    youtube:"https://youtube.com/@4cengresing",
    tiktok:"https://www.tiktok.com/@4cengresing"
  },

  {
    name:"Carlos Sutoyo",
    role:"Member",
    photo:"carlos-sutoyo.jpg",
    youtube:"https://youtube.com/@doleceling",
    tiktok:"https://www.tiktok.com/@sinyonyoxx"
  },

  {
    name:"Eichiro Oga Gian",
    role:"Prospect",
    photo:"eichiro-oga-gian.jpg",
    youtube:"https://youtube.com/@DAIGOXVIII",
    tiktok:"https://www.tiktok.com/@daigoxv"
  },

  {
    name:"Abraham Tax",
    role:"Prospect",
    photo:"abraham-tax.jpg",
    youtube:"https://youtube.com/@abrhmtax",
    tiktok:"https://www.tiktok.com/@nathanaelperkasa"
  },

  {
    name:"Lucas Louise",
    role:"Prospect",
    photo:"lucas-louise.jpg",
    youtube:"https://youtube.com/@GUNJOSJIS",
    tiktok:"https://www.tiktok.com/@jaydelucaa"
  },

  {
    name:"Gemi Crowave",
    role:"Prospect",
    photo:"gemi-crowave.jpg",
    youtube:"https://youtube.com/@gemiigaming",
    tiktok:"https://www.tiktok.com/@gemiiiiii"
  },

  {
    name:"Spencer D Rochefort",
    role:"Prospect",
    photo:"spencer-d-rochefort.jpg",
    youtube:"",
    tiktok:"https://www.tiktok.com/@ic.spencer"
  },

  {
    name:"Mya Rovert",
    role:"Prospect",
    photo:"mya-rovert.jpg",
    youtube:"https://youtube.com/@myarodrigo",
    tiktok:"https://www.tiktok.com/@itsmyarodrigo_"
  },

  {
    name:"Samsoel Patrick",
    role:"Prospect",
    photo:"samsoel-patrick.jpg",
    youtube:"https://youtube.com/@Samsoelpat",
    tiktok:"https://www.tiktok.com/@ic.samsoel6"
  }

];


/* =====================================================
   URUTAN JABATAN
===================================================== */

const ranks = [
  "Charter Veteran",
  "President",
  "Vice President",
  "Sergeant at Arms",
  "Road Captain",
  "Secretary",
  "Enforcer",
  "Member",
  "Prospect"
];


/* =====================================================
   RENDER MEMBER
===================================================== */

const container =
  document.getElementById("members-container");

function renderMembers(data){

  container.innerHTML = "";

  ranks.forEach((rank,index)=>{

    const list =
      data.filter(member => member.role === rank);

    if(!list.length) return;

    const rankBox =
      document.createElement("div");

    rankBox.className = "rank";

    rankBox.innerHTML = `
      <div class="rank-header">
        <div class="rank-number">${index + 1}</div>
        <h3>${rank}</h3>
      </div>

      <div class="member-grid"></div>
    `;

    const grid =
      rankBox.querySelector(".member-grid");

    list.forEach(member=>{

      const card =
        document.createElement("article");

      card.className = "member-card";

      const youtube = member.youtube
        ? `
          <a
            class="social yt"
            href="${member.youtube}"
            target="_blank"
            rel="noopener noreferrer"
          >
            ▶ YouTube
          </a>
        `
        : `
          <div class="unavailable">
            YouTube belum tersedia
          </div>
        `;

      const tiktok = member.tiktok
        ? `
          <a
            class="social tt"
            href="${member.tiktok}"
            target="_blank"
            rel="noopener noreferrer"
          >
            ♪ TikTok
          </a>
        `
        : `
          <div class="unavailable">
            TikTok belum tersedia
          </div>
        `;

      card.innerHTML = `

        <img
          class="member-photo"
          src="images/${member.photo}"
          alt="${member.name}"
          loading="lazy"
          onerror="this.src='images/logo-jdmc.png'"
        >

        <div class="member-content">

          <div class="member-name">
            ${member.name}
          </div>

          <div class="member-role">
            ${member.role}
          </div>

          <div class="socials">
            ${youtube}
            ${tiktok}
          </div>

        </div>
      `;

      grid.appendChild(card);

    });

    container.appendChild(rankBox);

  });

}


/* =====================================================
   INITIAL RENDER
===================================================== */

renderMembers(members);


/* =====================================================
   SEARCH
===================================================== */

const search =
  document.getElementById("search");

search.addEventListener("input",()=>{

  const keyword =
    search.value.toLowerCase().trim();

  const result =
    members.filter(member=>
      member.name.toLowerCase().includes(keyword) ||
      member.role.toLowerCase().includes(keyword)
    );

  renderMembers(result);

});


/* =====================================================
   FILTER
===================================================== */

document
.querySelectorAll(".filter")
.forEach(button=>{

  button.addEventListener("click",()=>{

    document
    .querySelectorAll(".filter")
    .forEach(btn=>
      btn.classList.remove("active")
    );

    button.classList.add("active");

    const filter =
      button.dataset.filter;

    search.value = "";

    if(filter === "all"){
      renderMembers(members);
      return;
    }

    renderMembers(
      members.filter(member=>
        member.role === filter
      )
    );

  });

});


/* =====================================================
   LOADING SCREEN
===================================================== */

window.addEventListener("load",()=>{

  setTimeout(()=>{

    document
    .getElementById("loader")
    .classList.add("hide");

  },700);

});

</script>

</body>
</html>          scroll-behavior: smooth;
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
