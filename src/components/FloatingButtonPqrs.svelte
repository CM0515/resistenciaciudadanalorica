<script>
  import { onMount } from "svelte";
  let modal;

  const openModal = () => {
    modal.showModal();
  };
</script>

<!-- Botón flotante -->
<button class="floating-button" on:click={openModal}> + </button>

<!-- Modal (usando <dialog> para accesibilidad y compatibilidad) -->
<dialog bind:this={modal} class="modal">
  <div class="modal-header">
    <h5>Formulario PQRS</h5>
    <button class="btn-close" on:click={() => modal.close()}>×</button>
  </div>
  <div class="modal-body">
    <!-- Formulario PQRS -->
    <form on:submit|preventDefault={() => alert("Formulario enviado!")}>
      <div class="mb-3">
        <label for="name" class="form-label">Nombre</label>
        <input
          type="text"
          class="form-control"
          id="name"
          placeholder="Tu nombre"
          required
        />
      </div>
      <div class="mb-3">
        <label for="email" class="form-label">Correo electrónico</label>
        <input
          type="email"
          class="form-control"
          id="email"
          placeholder="Tu correo"
          required
        />
      </div>
      <div class="mb-3">
        <label for="type" class="form-label">Tipo de PQRS</label>
        <select class="form-select" id="type" required>
          <option value="">Selecciona una opción</option>
          <option value="Petición">Petición</option>
          <option value="Queja">Queja</option>
          <option value="Reclamo">Reclamo</option>
          <option value="Sugerencia">Sugerencia</option>
        </select>
      </div>
      <div class="mb-3">
        <label for="message" class="form-label">Mensaje</label>
        <textarea
          class="form-control"
          id="message"
          rows="3"
          placeholder="Escribe tu mensaje"
          required
        ></textarea>
      </div>
      <button type="submit" class="btn btn-primary">Enviar</button>
    </form>
  </div>
</dialog>

<style>
  /* Botón flotante */
  .floating-button {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: rgb(5, 231, 254);
    color: white;
    border: none;
    border-radius: 50%;
    width: 60px;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    transition: all 0.3s ease;
    z-index: 1000;
  }

  .floating-button:hover {
    background-color: #039ea1;
    transform: scale(1.1);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.4);
  }

  /* Estilo del modal */
  .modal {
    padding: 20px;
    border-radius: 10px;
    border: none;
    max-width: 500px;
    margin: 20px auto;
    background-color: #fff;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
  }

  .modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .btn-close {
    background: none;
    border: none;
    font-size: 1.5rem;
  }

  .modal-body {
    margin-top: 20px;
  }

  form {
    display: flex;
    flex-direction: column;
  }

  .form-control {
    margin-bottom: 15px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }

  .btn-primary {
    background-color: #039ea1;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
</style>
