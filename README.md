<h1 align="center">Hola 👋, soy [Tu Nombre]</h1>

<!-- Loading animation -->
<div id="loading" align="center">
  <h2>Cargando...</h2>
</div>

<!-- Main content - initially hidden -->
<div id="main-content" style="display: none;">
  <!-- Promotional screen - animated image carousel -->
  <div id="carousel" align="center">
    <img id="promo-image" src="https://source.unsplash.com/random/800x400?tech" alt="Promocional" style="width:80%; border-radius:15px;" />
  </div>

  <!-- Blinking icons for tech stack -->
  <h2 align="center">Tecnologías que manejo 💻</h2>
  <div id="tech-icons" align="center">
    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
    <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white" />
    <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" />
    <img src="https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
    <img src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" />
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
    <img src="https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white" />
    <img src="https://img.shields.io/badge/Visual_Basic-5C2D91?style=for-the-badge&logo=microsoft&logoColor=white" />
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
    <img src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white" />
    <img src="https://img.shields.io/badge/Word-2B579A?style=for-the-badge&logo=microsoftword&logoColor=white" />
  </div>

  <!-- Personal description -->
  <h2 align="center">Sobre mí 😃</h2>
  <p align="center">
    Soy un entusiasta del mundo de la tecnología, actualmente estoy aprendiendo <strong>.NET, Angular, Python</strong> y <strong>Docker</strong>, 
    con un enfoque en bases de datos. Estoy estudiando para crear una pequeña empresa de software y tengo experiencia como freelancer en varios proyectos.
  </p>
</div>

<!-- Blinking animation for icons -->
<style>
  #loading h2 {
    animation: blink 1.5s infinite;
  }

  #tech-icons img {
    animation: blinkIcon 1.5s infinite alternate;
    margin: 10px;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  @keyframes blinkIcon {
    0% { opacity: 0.5; transform: scale(1); }
    100% { opacity: 1; transform: scale(1.1); }
  }

  #promo-image {
    animation: slide 5s infinite;
  }

  @keyframes slide {
    0% { transform: translateX(0); }
    50% { transform: translateX(100%); }
    100% { transform: translateX(0); }
  }
</style>

<!-- Script for loading and image slideshow -->
<script>
  document.addEventListener("DOMContentLoaded", function() {
    // Show main content after loading
    setTimeout(() => {
      document.getElementById('loading').style.display = 'none';
      document.getElementById('main-content').style.display = 'block';
    }, 3000); // 3-second loading delay

    // Image slideshow logic
    const images = [
      'https://source.unsplash.com/random/800x400?coding',
      'https://source.unsplash.com/random/800x400?technology',
      'https://source.unsplash.com/random/800x400?software'
    ];
    let currentImageIndex = 0;

    setInterval(() => {
      const promoImage = document.getElementById('promo-image');
      currentImageIndex = (currentImageIndex + 1) % images.length;
      promoImage.src = images[currentImageIndex];
    }, 5000); // Change image every 5 seconds
  });
</script>
