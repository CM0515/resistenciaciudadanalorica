<script>
  export let destacados = [];
</script>

<section>
  <div class="container">
    <div class="row">
      <div class="col-12">
        <div class="parche">
          <div class="titulo">
            <h1>Destacados</h1>
          </div>
          {#each destacados as destacado}
            <div class="destacado">
              <div class="row">
                <div class="col-12 col-sm-12 col-md-6">
                  <div class="imagen">
                    <a href={destacado.link} target="_blank">
                      <img
                        class="img-fluid"
                        src={destacado.image}
                        alt={destacado.title}
                      />
                    </a>
                  </div>
                </div>
                <div class="col-12 col-sm-12 col-md-6">
                  <h3 style="font-size: 38px;">
                    <a
                      style="font-size: 38px;"
                      href={destacado.link}
                      target="_blank"
                    >
                      {destacado.title}
                    </a>
                  </h3>
                  <p>{destacado.description}</p>
                  <small>
                    <span>{destacado.date}</span> |
                    <span>{destacado.source}</span>
                  </small>
                </div>
              </div>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .parche {
    margin-top: 20px;
  }

  /* Estilos para la imagen */
  .destacado .imagen img {
    width: 100%; /* Imagen toma todo el ancho del contenedor */
    height: auto; /* Mantiene la proporción de la imagen */
    max-height: 400px; /* Altura máxima de la imagen */
    object-fit: cover; /* Asegura que la imagen se ajuste dentro del contenedor */
    border-radius: 12px 0 0 12px; /* Bordes redondeados para la imagen */
  }


  .titulo h1 {
    font-size: 3em;
    text-align: center;
    margin-bottom: 30px;
  }

  .destacado {
    margin-bottom: 30px;
  }

  .imagen img {
    max-width: 100%;
    border-radius: 5px;
  }

  h3 a {
    color: #000;
    text-decoration: none;
  }

  h3 a:hover {
    color: #039ea1;
  }

  .destacado p {
    color: #666;
    line-height: 1.6;
    margin: 0 0 10px;
  }

  small {
    color: #999;
    font-size: 14px;
  }
</style>
