<script>
import PerfilUsuario from './components/PerfilUsuario.vue';
import Producto from './components/Producto.vue';
import FormularioUsuario from './components/FormularioUsuario.vue'
import ListaProductos from './components/ListaProductos.vue'
import NeoProducto from './components/NeoProducto.vue'

export default{
  name: 'App',
  components:{
    PerfilUsuario,Producto,FormularioUsuario,ListaProductos,NeoProducto,
  },
  data(){
    return{
      productos:[],
    }
  },
  methods:{
    agregarProducto(datosFormulario){
      this.productos.push(datosFormulario);
      console.log(this.productos);
    },
  }
}
</script>

<template>
  <PerfilUsuario/>
  <Producto/>
  <FormularioUsuario/>
  <div class="container">
    <NeoProducto @submit-form="agregarProducto"/>
    <ListaProductos :productos="productos"/>    
  </div>
</template>

<style scoped>

</style>
