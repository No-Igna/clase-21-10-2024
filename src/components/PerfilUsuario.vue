<!-- Ejercicio 1: Creación de un componente de tarjeta de perfil con Bootstrap
Crea un componente llamado PerfilUsuario.vue que muestre la información de un usuario, incluyendo su nombre, ocupación y una breve biografía. El diseño debe utilizar las tarjetas (card) de Bootstrap. Después, despliega el proyecto en GitHub Pages. -->

<template>
  <div class="container mt-3">
    <div class="card col-4">
      <div class="card-body">
        <h5 class="card-title"><strong>Nombre:</strong> {{ perfil.nombre }}</h5>
        <h6 class="card-subtitle mb-2 text-body-secondary"><strong>Ocupacion:</strong> {{ perfil.ocupacion }}</h6>
        <p class="card-text">{{ perfil.biografia }}</p>
      </div>
    </div>
  </div>
  <hr>
</template>

<script>
export default {
  name: 'PerfilUsuario',
  data() {
    return {
      perfil: {
        nombre: "sujeto de pruebas",
        ocupacion: "Ser el primer perfil creado",
        biografia: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit minima sint ad tempore, magni voluptatum sapiente unde rem ipsa laboriosam in dignissimos a libero perspiciatis obcaecati corrupti dolore provident rerum?"
      }
    };
  }
};
</script>

<style scoped></style>