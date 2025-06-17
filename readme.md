<!-- HEADER -->
<style>
  /* Smooth scrolling untuk seluruh halaman */
  html {
    scroll-behavior: smooth;
  }
  
  /* Optimasi performa untuk animasi */
  .tech-icon, .tailwind-animation, .bootstrap-animation, .database-animation, .framework-animation, .tool-animation {
    will-change: transform;
    transform: translateZ(0);
    backface-visibility: hidden;
  }
  
  /* Mengurangi animasi saat scrolling untuk performa lebih baik */
  .scrolling .tech-icon,
  .scrolling .tailwind-animation,
  .scrolling .bootstrap-animation,
  .scrolling .database-animation,
  .scrolling .framework-animation,
  .scrolling .tool-animation,
  .scrolling .float-animation,
  .scrolling .pulse-animation,
  .scrolling .spin-animation,
  .scrolling .shake-animation,
  .scrolling .bounce-animation {
    animation-play-state: paused !important;
  }
  
  /* Tambahan optimasi untuk smooth scrolling */
  body {
    overflow-x: hidden;
  }
  
  /* Mengurangi reflow dengan transform */
  .tech-icon, img, .container, .table {
    transform: translateZ(0);
  }
  
  /* Mengurangi jumlah animasi pada perangkat mobile */
  @media (max-width: 768px) {
    .float-animation, .pulse-animation, .spin-animation, .shake-animation, .bounce-animation {
      animation-duration: 4s !important; /* Lebih lambat untuk mengurangi CPU usage */
    }
    
    .delay-1, .delay-2, .delay-3, .delay-4, .delay-5, .delay-6 {
      animation-delay: 0s !important; /* Hapus delay pada mobile */
    }
  }
  
  /* Optimasi untuk perangkat dengan preferensi reduced motion */
  @media (prefers-reduced-motion: reduce) {
    *, ::before, ::after {
      animation-duration: 0.01ms !important;
      animation-iteration-count: 1 !important;
      transition-duration: 0.01ms !important;
      scroll-behavior: auto !important;
    }
  }
</style>

<script>
  // Deteksi scrolling untuk paused animasi saat scroll
  document.addEventListener('DOMContentLoaded', function() {
    let scrollingTimer;
    let isScrolling = false;
    
    window.addEventListener('scroll', function() {
      if (!isScrolling) {
        isScrolling = true;
        document.body.classList.add('scrolling');
      }
      
      clearTimeout(scrollingTimer);
      scrollingTimer = setTimeout(function() {
        isScrolling = false;
        document.body.classList.remove('scrolling');
      }, 200);
    });
  });
</script>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=header&text=Fadhli%20Rajwaa%20Rahmana&fontSize=70&animation=fadeIn&fontAlignY=38&desc=Fullstack%20Developer%20|%20Web%20Enthusiast%20|%20Code%20Artist&descAlignY=60&descAlign=50" width="100%">
</p>

<!-- 
  ANIMASI LOGO TEKNOLOGI
  
  Fitur Animasi yang Ditingkatkan:
  1. Setiap logo teknologi memiliki animasi yang berbeda (float, spin, bounce, shake, pulse)
  2. Logo React memiliki efek spin dan pulse khusus
  3. Logo TailwindCSS yang diperbaiki dengan efek gradient
  4. Logo Bootstrap baru dengan efek glow ungu
  5. Logo Database memiliki efek glow saat hover dengan warna sesuai database
  6. Logo Tools memiliki overlay informasi saat hover
  7. Logo CMS & Frameworks memiliki efek rotasi 3D dan partikel
  8. Bagian "Semua Teknologi" memiliki efek partikel dan border glow yang lebih menarik
  9. Semua logo memiliki efek hover 3D dan efek klik interaktif dengan partikel yang lebih banyak
  10. Efek gelombang (wave) pada semua logo setiap 10 detik
  11. Animasi acak pada logo setiap beberapa detik
  12. Efek sparkle saat hover pada setiap logo
  
  Interaksi:
  - Hover: Logo akan membesar, berputar dalam 3D, dan memunculkan sparkle
  - Klik: Logo akan memunculkan partikel berwarna sesuai dengan logo
  - Semua Teknologi: Efek hover yang membuat container terangkat dan border glow berwarna-warni
-->

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?lines=Halo+👋+Saya+Fadhli+Rajwaa+Rahmana;Fullstack+Developer+dari+Indonesia&font=Fira%20Code&center=true&width=580&height=70&duration=4000&pause=1000&color=58A6FF&background=FFFFFF00&vCenter=true&size=24&repeat=true" alt="Typing SVG">
</p>

<div align="center">
  <a href="mailto:fadhlirajwaarahmana@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail Badge" width="120px" />
  </a>&nbsp;
  <a href="https://linkedin.com/in/fadhli-rajwaa-rahmana" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge" width="150px" />
  </a>&nbsp;
  <a href="https://instagram.com/fadhli_rr" target="_blank">
    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram Badge" width="150px" />
  </a>&nbsp;
  <img src="https://komarev.com/ghpvc/?username=fadhlirajwaa&style=for-the-badge&color=brightgreen" alt="Profile Views" />
</div>

<style>
  .social-badge:hover {
    transform: translateY(-5px);
    transition: 0.3s;
  }

  /* Animasi untuk logo teknologi */
  @keyframes float {
    0% { transform: translateY(0px); }
    50% { transform: translateY(-10px); }
    100% { transform: translateY(0px); }
  }
  
  @keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
  }
  
  @keyframes spin {
    0% { transform: rotate(0deg); }
    50% { transform: rotate(180deg); }
    100% { transform: rotate(360deg); }
  }
  
  @keyframes shake {
    0% { transform: rotate(0deg); }
    25% { transform: rotate(5deg); }
    50% { transform: rotate(0deg); }
    75% { transform: rotate(-5deg); }
    100% { transform: rotate(0deg); }
  }
  
  @keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-15px); }
  }
  
  /* Animasi khusus untuk React */
  .react-logo-container {
    position: relative;
    width: 80px;
    height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .react-logo-container::before,
  .react-logo-container::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    border-radius: 50%;
    border: 2px solid #61dafb;
    opacity: 0;
  }
  
  .react-logo-container::before {
    animation: react-pulse 2s infinite;
  }
  
  .react-logo-container::after {
    animation: react-pulse 2s infinite 1s;
  }
  
  @keyframes react-pulse {
    0% { transform: scale(0.8); opacity: 0; }
    50% { opacity: 0.5; }
    100% { transform: scale(1.2); opacity: 0; }
  }
  
  .react-spin-animation {
    animation: react-spin 10s linear infinite;
  }
  
  @keyframes react-spin {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
  
  /* Animasi khusus untuk TailwindCSS */
  .tailwind-container {
    position: relative;
    width: 80px;
    height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: visible;
  }
  
  .tailwind-animation {
    animation: tailwind-float-rotate 6s ease-in-out infinite;
    filter: drop-shadow(0 0 3px rgba(56, 189, 248, 0.3));
  }
  
  @keyframes tailwind-float-rotate {
    0% { transform: translateY(0) rotate(0deg); }
    25% { transform: translateY(-5px) rotate(5deg); }
    50% { transform: translateY(0) rotate(0deg); }
    75% { transform: translateY(5px) rotate(-5deg); }
    100% { transform: translateY(0) rotate(0deg); }
  }
  
  .tailwind-container:hover .tailwind-animation {
    animation: tailwind-wind 2s ease-in-out infinite;
    filter: drop-shadow(0 0 8px rgba(56, 189, 248, 0.8));
  }
  
  @keyframes tailwind-wind {
    0% { transform: scale(1) rotate(0deg); }
    25% { transform: scale(1.1) rotate(5deg); }
    50% { transform: scale(1.15) rotate(0deg); }
    75% { transform: scale(1.1) rotate(-5deg); }
    100% { transform: scale(1) rotate(0deg); }
  }
  
  /* Animasi khusus untuk Bootstrap */
  .bootstrap-container {
    position: relative;
    width: 80px;
    height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }
  
  .bootstrap-animation {
    animation: bootstrap-pulse 2s ease-in-out infinite alternate;
  }
  
  @keyframes bootstrap-pulse {
    0% { transform: scale(1); filter: drop-shadow(0 0 0px rgba(113, 44, 249, 0)); }
    100% { transform: scale(1.1); filter: drop-shadow(0 0 10px rgba(113, 44, 249, 0.8)); }
  }
  
  .bootstrap-glow {
    position: absolute;
    width: 100%;
    height: 100%;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(113, 44, 249, 0.6) 0%, rgba(113, 44, 249, 0) 70%);
    opacity: 0;
    z-index: -1;
    transition: all 0.5s ease;
  }
  
  .bootstrap-container:hover .bootstrap-glow {
    opacity: 1;
    animation: bootstrap-glow 1.5s infinite alternate;
  }
  
  @keyframes bootstrap-glow {
    0% { transform: scale(0.8); opacity: 0.3; }
    100% { transform: scale(1.2); opacity: 0.7; }
  }
  
  /* Animasi untuk database */
  .database-container {
    position: relative;
    width: 80px;
    height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
  }
  
  .database-glow {
    position: absolute;
    width: 100%;
    height: 100%;
    border-radius: 50%;
    z-index: -1;
    filter: blur(10px);
    opacity: 0;
    transition: opacity 0.3s ease;
  }
  
  .database-container:hover .database-glow {
    opacity: 0.7;
    animation: glow-pulse 1.5s infinite alternate;
  }
  
  @keyframes glow-pulse {
    from { opacity: 0.3; transform: scale(0.9); }
    to { opacity: 0.7; transform: scale(1.1); }
  }
  
  .mongodb-glow {
    background-color: #4DB33D;
  }
  
  .mysql-glow {
    background-color: #00758F;
  }
  
  .postgresql-glow {
    background-color: #336791;
  }
  
  .database-animation {
    animation: database-float 3s ease-in-out infinite;
  }
  
  @keyframes database-float {
    0% { transform: translateY(0) scale(1); }
    50% { transform: translateY(-5px) scale(1.05); }
    100% { transform: translateY(0) scale(1); }
  }
  
  /* Animasi untuk CMS & Frameworks */
  .framework-container {
    position: relative;
    width: 80px;
    height: 80px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .framework-animation {
    animation: framework-rotate 8s ease-in-out infinite;
    filter: drop-shadow(0 0 5px rgba(255, 255, 255, 0.5));
  }
  
  @keyframes framework-rotate {
    0% { transform: rotateY(0deg); }
    50% { transform: rotateY(180deg); }
    100% { transform: rotateY(360deg); }
  }
  
  .framework-particles {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
  }
  
  .framework-container:hover .framework-particles::before,
  .framework-container:hover .framework-particles::after {
    content: '';
    position: absolute;
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(255,255,255,1) 0%, rgba(255,255,255,0) 70%);
    animation: particle-float 2s ease-in-out infinite;
  }
  
  .framework-container:hover .framework-particles::before {
    top: 20%;
    left: 20%;
    animation-delay: 0s;
  }
  
  .framework-container:hover .framework-particles::after {
    bottom: 20%;
    right: 20%;
    animation-delay: 0.5s;
  }
  
  @keyframes particle-float {
    0% { transform: translate(0, 0); opacity: 0; }
    50% { opacity: 1; }
    100% { transform: translate(20px, -20px); opacity: 0; }
  }
  
  /* Animasi untuk tools */
  .tool-container {
    position: relative;
    width: 80px;
    height: 80px;
    border-radius: 10px;
    overflow: hidden;
    margin: 0 auto;
  }
  
  .tool-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0;
    transition: opacity 0.3s ease;
  }
  
  .tool-container:hover .tool-overlay {
    opacity: 1;
  }
  
  .tool-info {
    color: white;
    font-size: 12px;
    font-weight: bold;
    text-align: center;
    transform: translateY(20px);
    transition: transform 0.3s ease;
  }
  
  .tool-container:hover .tool-info {
    transform: translateY(0);
  }
  
  .tool-animation {
    animation: tool-bounce 2s ease infinite;
  }
  
  @keyframes tool-bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-5px); }
  }
  
  .tool-container:hover .tech-icon {
    transform: scale(1.1) rotate(5deg);
  }
  
  /* Tambahan animasi 3D untuk ikon teknologi */
  .all-tech-container {
    perspective: 1000px;
    transition: transform 0.5s;
    margin: 20px 0;
    position: relative;
    padding: 20px;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    background: rgba(13, 17, 23, 0.3);
  }
  
  .all-tech-container::before {
    content: '';
    position: absolute;
    top: -10px;
    left: -10px;
    right: -10px;
    bottom: -10px;
    border-radius: 10px;
    background: linear-gradient(45deg, #12c2e9, #c471ed, #f64f59, #7303c0, #ec38bc, #fdeff9);
    background-size: 400% 400%;
    z-index: -1;
    opacity: 0;
    transition: opacity 0.5s;
    animation: gradient-shift 15s ease infinite;
  }
  
  @keyframes gradient-shift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }
  
  .all-tech-container:hover::before {
    opacity: 0.6;
  }
  
  .all-tech-container:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.3);
  }
  
  /* Efek 3D hover untuk ikon teknologi */
  .tech-icon {
    transition: all 0.3s ease;
    transform-style: preserve-3d;
    position: relative;
    z-index: 2;
    filter: drop-shadow(0 5px 15px rgba(0,0,0,0.1));
  }
  
  .tech-icon:hover {
    transform: scale(1.3) rotateY(15deg) translateZ(20px);
    filter: drop-shadow(0 0 15px rgba(0, 123, 255, 0.8));
  }
  
  /* Efek partikel yang lebih menarik */
  .tech-particles {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 1;
    overflow: hidden;
  }
  
  .particle {
    position: absolute;
    background: radial-gradient(circle, rgba(255,255,255,0.8) 0%, rgba(255,255,255,0) 70%);
    border-radius: 50%;
    pointer-events: none;
    opacity: 0;
    z-index: 1;
  }
  
  @keyframes float-up {
    0% { transform: translateY(100px) rotate(0deg); opacity: 0; }
    10% { opacity: 1; }
    90% { opacity: 0.7; }
    100% { transform: translateY(-100px) rotate(360deg); opacity: 0; }
  }
  
  @keyframes sparkle {
    0%, 100% { opacity: 0; transform: scale(0); }
    50% { opacity: 1; transform: scale(1); }
  }
  
  .sparkle {
    position: absolute;
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background-color: white;
    pointer-events: none;
    animation: sparkle 1s ease-in-out infinite;
  }
  
  .float-animation {
    animation: float 3s ease-in-out infinite;
  }
  
  .pulse-animation {
    animation: pulse 2s ease-in-out infinite;
  }
  
  .spin-animation {
    animation: spin 8s linear infinite;
  }
  
  .shake-animation {
    animation: shake 3s ease-in-out infinite;
  }
  
  .bounce-animation {
    animation: bounce 2s ease infinite;
  }
  
  .delay-1 {
    animation-delay: 0.2s;
  }
  
  .delay-2 {
    animation-delay: 0.4s;
  }
  
  .delay-3 {
    animation-delay: 0.6s;
  }
  
  .delay-4 {
    animation-delay: 0.8s;
  }
  
  .delay-5 {
    animation-delay: 1s;
  }
  
  .delay-6 {
    animation-delay: 1.2s;
  }
  
  /* Mengurangi animasi saat scrolling untuk performa lebih baik */
  @media screen and (prefers-reduced-motion: no-preference) {
    .scrolling .tech-icon {
      animation-play-state: paused;
    }
  }
  
  /* Mengoptimalkan animasi dengan hardware acceleration */
  .float-animation, .pulse-animation, .spin-animation, .shake-animation, .bounce-animation {
    transform: translate3d(0, 0, 0);
    backface-visibility: hidden;
    perspective: 1000px;
  }
</style>

<!-- ABOUT ME SECTION -->
## 🚀 Tentang Saya

<img align="right" src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="200">

```javascript
const fadhli = {
  pronouns: "Dia/Dia",
  code: ["JavaScript", "TypeScript", "HTML", "CSS", "Python", "Java", "PHP", "Kotlin"],
  askMeAbout: ["web dev", "tech", "app dev"],
  technologies: {
    frontEnd: {
      js: ["React"],
      css: ["Tailwind CSS"]
    },
    backEnd: {
      js: ["Node", "Express"],
      php: ["WordPress"]
    },
    databases: ["MongoDB", "MySQL", "PostgreSQL"]
  },
  currentFocus: "Mengembangkan Aplikasi Web Full Stack",
  funFact: "Bugs dan kopi adalah bagian dari kehidupan programmer"
};
```

<!-- SKILLS SECTION -->
## 💻 Tech Stack

<!-- Frontend -->
<h3 align="center">Frontend</h3>
<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" width="80" height="80" alt="JavaScript" class="tech-icon float-animation"/>
          <br />JavaScript
        </a>
      </td>
      <td align="center">
        <a href="https://www.typescriptlang.org/">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" width="80" height="80" alt="TypeScript" class="tech-icon float-animation delay-1"/>
          <br />TypeScript
        </a>
      </td>
      <td align="center">
        <a href="https://reactjs.org/">
          <div class="react-logo-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" width="80" height="80" alt="React" class="tech-icon react-spin-animation"/>
          </div>
          <br />React
        </a>
      </td>
      <td align="center">
        <a href="https://developer.mozilla.org/en-US/docs/Web/HTML">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" width="80" height="80" alt="HTML5" class="tech-icon float-animation delay-2"/>
          <br />HTML5
        </a>
      </td>
      <td align="center">
        <a href="https://developer.mozilla.org/en-US/docs/Web/CSS">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" width="80" height="80" alt="CSS3" class="tech-icon float-animation delay-3"/>
          <br />CSS3
        </a>
      </td>
      <td align="center">
        <a href="https://tailwindcss.com/">
          <div class="tailwind-container">
            <img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" width="80" height="80" alt="TailwindCSS" class="tech-icon tailwind-animation"/>
          </div>
          <br />TailwindCSS
        </a>
      </td>
      <td align="center">
        <a href="https://getbootstrap.com/">
          <div class="bootstrap-container">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" width="80" height="80" alt="Bootstrap" class="tech-icon bootstrap-animation"/>
            <div class="bootstrap-glow"></div>
          </div>
          <br />Bootstrap
        </a>
      </td>
    </tr>
  </table>
</div>

<!-- Backend -->
<h3 align="center">Backend</h3>
<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://nodejs.org/">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" width="80" height="80" alt="NodeJS" class="tech-icon shake-animation"/>
          <br />Node.js
        </a>
      </td>
      <td align="center">
        <a href="https://expressjs.com/">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" width="80" height="80" alt="Express" class="tech-icon pulse-animation delay-1"/>
          <br />Express
        </a>
      </td>
      <td align="center">
        <a href="https://www.php.net/">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" width="80" height="80" alt="PHP" class="tech-icon bounce-animation"/>
          <br />PHP
        </a>
      </td>
      <td align="center">
        <a href="https://www.java.com/">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" width="80" height="80" alt="Java" class="tech-icon bounce-animation delay-1"/>
          <br />Java
        </a>
      </td>
      <td align="center">
        <a href="https://www.python.org/">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" width="80" height="80" alt="Python" class="tech-icon bounce-animation delay-2"/>
          <br />Python
        </a>
      </td>
      <td align="center">
        <a href="https://kotlinlang.org/">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/kotlin/kotlin-original.svg" width="80" height="80" alt="Kotlin" class="tech-icon bounce-animation delay-3"/>
          <br />Kotlin
        </a>
      </td>
    </tr>
  </table>
</div>

<!-- CMS & Frameworks -->
<h3 align="center">CMS & Frameworks</h3>
<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://wordpress.org/">
          <div class="framework-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/wordpress/wordpress-original.svg" width="80" height="80" alt="WordPress" class="tech-icon framework-animation"/>
            <div class="framework-particles"></div>
          </div>
          <br />WordPress
        </a>
      </td>
      <td align="center">
        <a href="https://nextjs.org/">
          <div class="framework-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nextjs/nextjs-original.svg" width="80" height="80" alt="Next.js" class="tech-icon framework-animation delay-1"/>
            <div class="framework-particles"></div>
          </div>
          <br />Next.js
        </a>
      </td>
    </tr>
  </table>
</div>

<!-- Database -->
<h3 align="center">Database</h3>
<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://www.mongodb.com/">
          <div class="database-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" width="80" height="80" alt="MongoDB" class="tech-icon database-animation"/>
            <div class="database-glow mongodb-glow"></div>
          </div>
          <br />MongoDB
        </a>
      </td>
      <td align="center">
        <a href="https://www.mysql.com/">
          <div class="database-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" width="80" height="80" alt="MySQL" class="tech-icon database-animation delay-1"/>
            <div class="database-glow mysql-glow"></div>
          </div>
          <br />MySQL
        </a>
      </td>
      <td align="center">
        <a href="https://www.postgresql.org/">
          <div class="database-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" width="80" height="80" alt="PostgreSQL" class="tech-icon database-animation delay-2"/>
            <div class="database-glow postgresql-glow"></div>
          </div>
          <br />PostgreSQL
        </a>
      </td>
    </tr>
  </table>
</div>

<!-- Tools -->
<h3 align="center">Tools</h3>
<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://git-scm.com/">
          <div class="tool-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" width="80" height="80" alt="Git" class="tech-icon tool-animation"/>
            <div class="tool-overlay">
              <div class="tool-info">Version Control</div>
            </div>
          </div>
          <br />Git
        </a>
      </td>
      <td align="center">
        <a href="https://code.visualstudio.com/">
          <div class="tool-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vscode/vscode-original.svg" width="80" height="80" alt="VS Code" class="tech-icon tool-animation delay-1"/>
            <div class="tool-overlay">
              <div class="tool-info">Code Editor</div>
            </div>
          </div>
          <br />VS Code
        </a>
      </td>
      <td align="center">
        <a href="https://developer.android.com/studio">
          <div class="tool-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original.svg" width="80" height="80" alt="Android Studio" class="tech-icon tool-animation delay-2"/>
            <div class="tool-overlay">
              <div class="tool-info">Mobile Dev</div>
            </div>
          </div>
          <br />Android Studio
        </a>
      </td>
      <td align="center">
        <a href="https://www.docker.com/">
          <div class="tool-container">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" width="80" height="80" alt="Docker" class="tech-icon tool-animation delay-3"/>
            <div class="tool-overlay">
              <div class="tool-info">Containerization</div>
            </div>
          </div>
          <br />Docker
        </a>
      </td>
    </tr>
  </table>
</div>

<!-- Semua Teknologi dengan Animasi -->
<div align="center">
  <h3>Semua Teknologi</h3>
  <div class="all-tech-container">
    <div class="tech-particles"></div>
    <img src="https://skillicons.dev/icons?i=js,ts,react,html,css,tailwind,bootstrap,nodejs,express,php,wordpress,laravel,nextjs,java,kotlin,python,mongodb,mysql,postgresql,git,vscode,androidstudio,docker&perline=12" alt="Semua Tech Stack" class="tech-icon pulse-animation" />
  </div>
</div>

<script>
  // Fungsi untuk mengoptimalkan performa dengan throttling
  document.addEventListener('DOMContentLoaded', function() {
    // Throttle function untuk membatasi frekuensi eksekusi fungsi
    const throttle = (func, limit) => {
      let inThrottle;
      return function() {
        const args = arguments;
        const context = this;
        if (!inThrottle) {
          func.apply(context, args);
          inThrottle = true;
          setTimeout(() => inThrottle = false, limit);
        }
      };
    };
    
    // Fungsi untuk membuat partikel dengan performa yang lebih baik
    const createOptimizedParticles = (element, count, colors) => {
      // Buat partikel hanya jika perangkat cukup kuat
      const isLowPowerDevice = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
      if (isLowPowerDevice) {
        return; // Tidak membuat partikel pada perangkat dengan daya rendah
      }
      
      // Batasi jumlah partikel berdasarkan performa perangkat
      const particleCount = window.innerWidth < 768 ? Math.min(count, 5) : count;
      
      const container = element.parentNode;
      const rect = element.getBoundingClientRect();
      
      // Gunakan fragment untuk mengurangi reflow
      const fragment = document.createDocumentFragment();
      
      for (let i = 0; i < particleCount; i++) {
        const particle = document.createElement('div');
        
        // Ukuran acak
        const size = Math.random() * 5 + 2;
        particle.style.width = size + 'px';
        particle.style.height = size + 'px';
        
        // Posisi awal di tengah elemen
        particle.style.position = 'absolute';
        particle.style.left = '50%';
        particle.style.top = '50%';
        
        // Styling
        particle.style.borderRadius = '50%';
        particle.style.pointerEvents = 'none';
        
        // Warna acak dari array colors
        const color = colors[Math.floor(Math.random() * colors.length)];
        particle.style.backgroundColor = color;
        
        // Arah acak
        const angle = Math.random() * Math.PI * 2;
        const distance = 20 + Math.random() * 20;
        const x = Math.cos(angle) * distance;
        const y = Math.sin(angle) * distance;
        
        // Animasi dengan CSS transform untuk performa lebih baik
        particle.style.transform = 'translate(-50%, -50%)';
        particle.style.opacity = '0';
        particle.style.transition = 'transform 1s ease-out, opacity 1s ease-out';
        
        // Tambahkan ke fragment
        fragment.appendChild(particle);
        
        // Mulai animasi di frame berikutnya untuk menghindari layout thrashing
        requestAnimationFrame(() => {
          particle.style.transform = `translate(calc(-50% + ${x}px), calc(-50% + ${y}px))`;
          particle.style.opacity = '0.7';
          
          // Fade out
          setTimeout(() => {
            particle.style.opacity = '0';
          }, 500);
          
          // Hapus partikel setelah animasi selesai
          setTimeout(() => {
            if (particle.parentNode) {
              particle.parentNode.removeChild(particle);
            }
          }, 1000);
        });
      }
      
      // Tambahkan semua partikel sekaligus untuk mengurangi reflow
      container.appendChild(fragment);
    };
    
    // Optimalkan efek hover pada logo TailwindCSS
    const tailwindLogo = document.querySelector('.tailwind-container img');
    if (tailwindLogo) {
      const optimizedHoverHandler = throttle(() => {
        createOptimizedParticles(tailwindLogo, 8, ['#06B6D4', '#0EA5E9', '#38BDF8', '#7DD3FC']);
      }, 300);
      
      tailwindLogo.addEventListener('mouseenter', optimizedHoverHandler);
    }
    
    // Optimalkan animasi wave dengan requestAnimationFrame
    const createWaveEffect = () => {
      const techIcons = document.querySelectorAll('.tech-icon');
      if (!techIcons.length) return;
      
      // Jangan jalankan animasi jika halaman tidak terlihat atau scrolling
      if (document.hidden || document.body.classList.contains('scrolling')) {
        return;
      }
      
      let index = 0;
      const animateNext = () => {
        if (index >= techIcons.length) return;
        
        const icon = techIcons[index];
        icon.classList.add('bounce-animation');
        
        setTimeout(() => {
          icon.classList.remove('bounce-animation');
          index++;
          requestAnimationFrame(animateNext);
        }, 100);
      };
      
      requestAnimationFrame(animateNext);
    };
    
    // Jalankan wave effect setiap 15 detik, tapi hanya jika halaman terlihat
    let waveInterval;
    const startWaveInterval = () => {
      waveInterval = setInterval(() => {
        if (!document.hidden && !document.body.classList.contains('scrolling')) {
          createWaveEffect();
        }
      }, 15000);
    };
    
    // Mulai interval
    startWaveInterval();
    
    // Pause animasi saat tab tidak aktif
    document.addEventListener('visibilitychange', () => {
      if (document.hidden) {
        clearInterval(waveInterval);
      } else {
        startWaveInterval();
      }
    });
  });
</script>

<!-- STATS SECTION -->
## 📊 GitHub Stats

<div align="center">
  <p>
    <a href="https://github.com/fadhlirajwaa">
      <img src="https://github-readme-stats.vercel.app/api?username=fadhlirajwaa&show_icons=true&count_private=true&hide_border=true&theme=radical&bg_color=0D1117&title_color=C9D1D9&icon_color=58A6FF&text_color=8B949E&ring_color=58A6FF" width="48%" />
    </a>
    <a href="https://github.com/fadhlirajwaa">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=fadhlirajwaa&hide_border=true&theme=radical&background=0D1117&stroke=0D1117&ring=58A6FF&fire=58A6FF&currStreakLabel=58A6FF" width="48%" />
    </a>
  </p>
  <p>
    <a href="https://github.com/fadhlirajwaa">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=fadhlirajwaa&layout=compact&hide_border=true&theme=radical&bg_color=0D1117&title_color=C9D1D9&text_color=8B949E" />
    </a>
  </p>
</div>

<!-- TROPHY SECTION -->
<div align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=fadhlirajwaa&theme=radical&column=7&margin-w=15&rank=SSS,SS,S,AAA,AA,A,B,C" alt="GitHub Trophies" />
</div>

<!-- SNAKE ANIMATION -->
<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake.svg" />
    <img alt="GitHub contribution grid snake animation" src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake.svg" />
  </picture>
</div>

<!-- ACTIVITY GRAPH -->
<div align="center">
  <br/>
  <a href="https://github.com/fadhlirajwaa">
    <img alt="Fadhli's Activity Graph" src="https://github-readme-activity-graph.vercel.app/graph?username=fadhlirajwaa&bg_color=0D1117&color=5BCDEC&line=5BCDEC&point=FFFFFF&hide_border=true" width="98%" />
  </a>
</div>

<!-- QUOTE SECTION -->
## 💭 Quotes Programmer Favorit

<div align="center">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical" alt="Programming Quote" />
</div>

---

<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?lines=Terima+kasih+telah+mengunjungi+profil+saya!;Mari+terhubung+dan+berkolaborasi!&font=Fira%20Code&center=true&width=580&height=70&duration=4000&pause=1000&color=58A6FF&background=FFFFFF00&vCenter=true&size=24&repeat=true" alt="Typing SVG">

  <p>
    <a href="https://github.com/fadhlirajwaa">
      <img alt="GitHub followers" src="https://img.shields.io/github/followers/fadhlirajwaa?style=for-the-badge&logo=github&logoColor=white&label=FOLLOW&labelColor=black&color=blue" />
    </a>
  </p>
  
  <br/>
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=120&section=footer&animation=fadeIn" width="100%"/>
</div>

<script>
  // Deteksi perangkat dengan performa rendah dan secara otomatis mengurangi efek animasi
  document.addEventListener('DOMContentLoaded', function() {
    // Deteksi perangkat dengan performa rendah
    const detectLowPowerDevice = () => {
      // Deteksi berdasarkan user agent (mobile)
      const isMobile = /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
      
      // Deteksi berdasarkan preferensi reduced motion
      const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
      
      // Deteksi berdasarkan jumlah core CPU (jika tersedia)
      const lowCPU = navigator.hardwareConcurrency && navigator.hardwareConcurrency <= 4;
      
      // Deteksi berdasarkan memori (jika tersedia)
      const lowMemory = navigator.deviceMemory && navigator.deviceMemory <= 4;
      
      return isMobile || prefersReducedMotion || lowCPU || lowMemory;
    };
    
    // Jika perangkat memiliki performa rendah, kurangi animasi
    if (detectLowPowerDevice()) {
      document.body.classList.add('reduce-animations');
      
      // Kurangi animasi
      const reducedAnimations = `
        .float-animation, .pulse-animation, .spin-animation, .shake-animation, .bounce-animation,
        .tailwind-animation, .bootstrap-animation, .database-animation, .framework-animation, .tool-animation {
          animation-duration: 5s !important;
          animation-delay: 0s !important;
        }
        
        .particle, .sparkle, .framework-particles, .tech-particles {
          display: none !important;
        }
      `;
      
      // Tambahkan style untuk mengurangi animasi
      const style = document.createElement('style');
      style.textContent = reducedAnimations;
      document.head.appendChild(style);
      
      // Nonaktifkan interval animasi yang tidak perlu
      clearInterval(window.waveInterval);
      clearInterval(window.randomAnimationInterval);
    }
  });
</script>
