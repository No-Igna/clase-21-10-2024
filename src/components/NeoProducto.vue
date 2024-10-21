<template>
  <form @submit.prevent="submitProduct">
    <div class="mb-3">
      <label for="nombreID" class="form-label">Nombre producto:</label>
      <input type="text" class="form-control" id="nombreID" v-model="form.nombre" required>
    </div>
    <div class="mb-3">
      <label for="precioID" class="form-label">Precio producto:</label>
      <input type="number" class="form-control" id="precioID" v-model="form.precio" required>
    </div>
    <button type="submit" class="btn btn-primary">Agregar</button>
  </form>
  <hr>
</template>

<script>
export default {
  name: 'NeoProducto',
  data() {
    return {
      form: {
        nombre: "",
        precio: ""
      },
    };
  },
  methods: {
    submitProduct() {
      this.$emit('submit-form', this.form);
      this.form = {
        nombre: "",
        precio: ""
      }
    }
  }
};
</script>

<style scoped></style>