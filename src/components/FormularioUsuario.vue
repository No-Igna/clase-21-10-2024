<!-- Ejercicio 3: Formulario interactivo con Bootstrap y v-model
Crea un componente llamado FormularioUsuario.vue que tenga dos campos de entrada donde el usuario pueda ingresar su nombre y su edad, utilizando v-model. Muestra los valores ingresados en tiempo real. Usa el sistema de formularios de Bootstrap y despliega el proyecto en GitHub Pages. -->
<template>
  <div class="container mt-3">
    <div class="row">
      <form class="col-4">
        <div class="mb-3">
          <label for="nombreUsuario" class="form-label">Ingresar nombre</label>
          <input type="text" class="form-control" id="nombreUsuario" v-model="nombre">
        </div>
        <div class="mb-3">
          <label for="edadUsuario" class="form-label">Ingresar edad</label>
          <input type="number" class="form-control" id="edadUsuario" v-model="edad">
        </div>
      </form>
      <div class="col-4">
        <p v-if="nombre">Hola {{ nombre }}</p>
        <p v-if="edad">la edad ingresada es: {{ edad }}</p>
      </div>
    </div>
  </div>
  <hr>
</template>

<script>
export default {
  name: 'FormularioUsuario',
  data() {
    return {
      nombre:"",
      edad:""
    };
  }
};
</script>

<style scoped></style>