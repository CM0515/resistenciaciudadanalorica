<script>
  export let links = [];
</script>

<nav class="navbar navbar-expand-lg">
  <div class="container">
    <!-- Logo -->
    <a class="navbar-brand" href="/">
      <img src="/assets/img/logo.png" alt="Logo" class="logo" />
    </a>

    <!-- Botón de colapso para móviles -->
    <button
      class="navbar-toggler btn-light"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>

    <!-- Links del menú -->
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        {#each links as link}
          <li class="nav-item">
            <a class="nav-link" href={link.href}>{link.name}</a>
          </li>
        {/each}
      </ul>
    </div>
  </div>
</nav>

<style>
  .navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.4); /* Fondo transparente */
    padding: 15px;
    z-index: 100;
  }
  

  /* Estilos para el logo */
  .logo {
    height: 120px; /* Ajusta el tamaño del logo según sea necesario */
    width: auto;
  }

  /* Estilos del menú */
  .navbar ul {
    list-style-type: none;
    display: flex;
    justify-content: center;
  }

  .navbar ul li {
    margin: 0 20px;
  }

  .navbar ul li a {
    color: #fff;
    text-decoration: none;
    font-size: 18px;
    transition: color 0.3s ease;
  }

  .navbar ul li a:hover {
    color: #44ca46; /* Color principal para el efecto hover */
  }
</style>
