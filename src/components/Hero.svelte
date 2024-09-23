<!-- Sección de video con texto -->
<section class="hero">
  <video autoplay muted loop id="background-video">
    <source src="assets/videos/Fondo.mp4" type="video/mp4" />
    Tu navegador no soporta la reproducción de videos.
  </video>
  <div class="hero-text">
    <h1>TRABAJANDO POR LORICA</h1>
  </div>
</section>

<style>
  /* Sección de video con texto */
  .hero {
    position: relative;
    height: 100vh;
    overflow: hidden;
  }

  #background-video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .hero-text {
    position: relative;
    z-index: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
  }

  .hero-text h1 {
    color: #fff;
    font-size: 4em;
    text-align: center;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
    letter-spacing: 3px;
  }
</style>
