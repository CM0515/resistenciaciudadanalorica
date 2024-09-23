<script>
  // Obtener el año dinámicamente
  let currentYear = new Date().getFullYear();
</script>

<footer class="footer">
  <div class="container">
    <div class="text">
      <p>
        © {currentYear} Resistencia ciudadana | Todos los derechos reservados.
      </p>
    </div>
    <div class="social-icons">
      <a href="https://www.facebook.com" target="_blank" aria-label="Facebook">
        <i class="fab fa-facebook"></i>
      </a>
      <a
        href="https://www.instagram.com"
        target="_blank"
        aria-label="Instagram"
      >
        <i class="fab fa-instagram"></i>
      </a>
      <a href="https://twitter.com" target="_blank" aria-label="X (Twitter)">
        <i class="fab fa-x-twitter"></i>
      </a>
    </div>
  </div>
</footer>

<style>
  .footer {
    background-color: #333;
    color: #fff;
    padding: 20px 0;
    text-align: center;
  }

  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .text p {
    margin: 0;
    font-size: 1em;
  }

  .social-icons {
    margin-top: 10px;
  }

  .social-icons a {
    margin: 0 10px;
    color: #fff;
    font-size: 1.5em;
    transition: color 0.3s ease;
  }

  .social-icons a:hover {
    color: #039ea1; /* Cambiar color al pasar sobre el ícono */
  }
</style>

