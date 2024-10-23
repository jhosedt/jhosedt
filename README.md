<h1 align="center">Hola 👋, soy jhosedt</h1>

<div id="main-content">
  <!-- Promotional screen - animated image carousel -->
  <div id="carousel" align="center">
    <img id="promo-image" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTj8r_zQGxyzANwOl_HhdwBhbXGWShjhCy6Rf2SVgbnherHmNeUjMU8wtDVKsmHWm8L4A8&usqp=CAU"
    src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTj8r_zQGxyzANwOl_HhdwBhbXGWShjhCy6Rf2SVgbnherHmNeUjMU8wtDVKsmHWm8L4A8&usqp=CAU" alt="Promocional" />
    
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

<!-- CSS for hover effects and styling -->
<style>
  /* Style for the carousel */
  #carousel {
    overflow: hidden;
    position: relative;
    width: 80%; /* Asegúrate de que esto coincida con el ancho de la imagen */
    margin: 0 auto; /* Centrar el carrusel */
  }

  #promo-image {
    width: 100%;
    border-radius: 50% 51px;
    position: absolute; /* Asegúrate de que la imagen esté en una posición absoluta para moverla */
    transition: transform 1s ease; /* Añade la transición */
  }

  /* Style for the project cards */
  .card {
    width: 300px;
    border: 2px solid #f0f0f0;
    border-radius: 15px;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
    text-align: center;
  }

  .card:hover {
    transform: scale(1.05);
    box-shadow: 0px 10px 15px rgba(0, 0, 0, 0.1);
  }

  .card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  .card .details {
    padding: 15px;
  }

  .card .details h3 {
    margin: 10px 0;
    font-size: 1.5em;
    color: #333;
  }

  .card .details p {
    color: #777;
  }

  .card:hover img {
    transform: rotate(5deg);
    transition: transform 0.3s ease;
  }

  #tech-icons img {
    animation: blinkIcon 1.5s infinite alternate;
    margin: 10px;
  }

  @keyframes blinkIcon {
    0% { opacity: 0.5; transform: scale(1); }
    100% { opacity: 1; transform: scale(1.1); }
  }
</style>

<!-- Script for image slideshow -->
<script>
  document.addEventListener("DOMContentLoaded", function() {
    const images = [
      'https://source.unsplash.com/random/800x400?coding',
      'https://source.unsplash.com/random/800x400?technology',
      'https://source.unsplash.com/random/800x400?software'
    ];
    let currentImageIndex = 0;

    setInterval(() => {
      const promoImage = document.getElementById('promo-image');
      currentImageIndex = (currentImageIndex + 1) % images.length;

      // Cambiar la posición de la imagen
      promoImage.style.transform = `translateX(${100 * currentImageIndex}%)`;
      promoImage.src = images[currentImageIndex];
    }, 5000); // Cambiar imagen cada 5 segundos
  });
</script>
