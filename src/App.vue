<template>
  <CrearTarea msg="Crear una nueva tarea"/>
  <Formulario/>
</template>

<script>
import CrearTarea from '@/components/CrearTarea.vue';
import Formulario from '@/components/Formulario.vue';


export default {
  name: 'App',
  components: {
    CrearTarea,
    Formulario
  }
}
</script>

<style>
#app {
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #315f8d;
  margin-top: 80px;
}
</style>
