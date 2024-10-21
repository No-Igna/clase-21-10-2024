<template>
  <div v-if="productos.length" class="container mt-3">
    <div class="row">
      <div class="card col-4" v-for="(producto, index) in productos" :key="index">
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Nombre: {{ producto.nombre }}</li>
          <li class="list-group-item">Precio: {{ producto.precio }}</li>
        </ul>
      </div>
    </div>
    <hr>
  </div>
</template>

<script>
export default {
  name: 'ListaProductos',
  props:{
    productos: Array,
  },
  data() {
    return {};
  }
};
</script>

<style scoped></style>