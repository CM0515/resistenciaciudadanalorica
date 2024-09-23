<script>
  export let colaboradores = [];
</script>

<section class="colaboradores">
  <div class="container">
    <div class="titulo">
      <h2>Colaboradores y Patrocinadores</h2>
    </div>
    <div class="grid">
      {#each colaboradores as colaborador}
        <div class="colaborador">
          <a href={colaborador.link} target="_blank">
            <img src={colaborador.logo} alt={colaborador.name} />
          </a>
        </div>
        
        <h3>{colaborador.name}</h3>
      {/each}
    </div>
  </div>
</section>

<style>
  .colaboradores {
    padding: 80px 20px;
    background-color: #f0f0f0;
    text-align: center;
  }

  .titulo h2 {
    font-size: 2.5em;
    margin-bottom: 50px;
    color: #333;
    font-weight: 600;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 30px;
    justify-items: center;
    align-items: center;
  }

  .colaborador {
    background-color: rgba(255, 255, 255, 0.8);
    padding: 20px;
    border-radius: 12px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  }

  .colaborador:hover {
    transform: translateY(-10px);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
  }

  .colaborador img {
    max-width: 100%;
    height: auto;
    max-height: 100px;
    object-fit: contain;
    transition: transform 0.3s ease;
  }

  .colaborador:hover img {
    transform: scale(1.05);
  }
</style>
