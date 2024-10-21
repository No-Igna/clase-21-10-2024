<!-- Ejercicio 2: Uso de data bindings y Bootstrap
Crea un componente llamado Producto.vue que muestre el nombre y el precio de un producto. Además, cambia dinámicamente el color del texto del precio utilizando v-bind y usa componentes de Bootstrap, como una lista (list-group). Asegúrate de desplegar el proyecto en GitHub. -->

<template>
  <div class="container mt-3">
    <div class="card col-4">
      <ul class="list-group list-group-flush">
        <li class="list-group-item" :style="{ color: colorDinamico }"><strong>Nombre del producto: </strong>{{ producto.nombre }}</li>
        <li class="list-group-item"><strong>Precio: </strong>{{ producto.precio }}</li>
      </ul>
    </div>
    <select class="form-select mt-3" aria-label="Default select example" v-model="colorDinamico">
      <option value="" selected disabled>Elija un color</option>
      <option value="red">rojo</option>
      <option value="blue">azul</option>
      <option value="green">verde</option>
    </select>
  </div>
  <hr>
</template>

<script>
export default {
  name: 'Producto',
  data() {
    return {
      producto: {
        nombre: "producto de prueba",
        precio: "incalculable"
      },
      colorDinamico: ""
    };
  }
};
</script>

<style scoped></style>