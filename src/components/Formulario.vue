<template>
  <div class="formulario">
    <label for="input">Tarea: </label>
    <input id="input" type="text" placeholder="Ingresa una nueva tarea" v-model="nuevaLista">
    <button @click="AgregarTarea">Crear</button>
    <h3>Lista</h3>
    <ul>
      <li v-for="(lista, index) in agregar" :key="index"> 
          {{ index }}: {{lista}}
      </li>
    </ul>
  </div>
</template>

<script>
 export default {
    name: 'Formulario',
    data: () => ({
      nuevaLista: "",
      agregar: []
     
    }),
    methods: {
      AgregarTarea() {
        this.agregar.push(this.nuevaLista);
        this.nuevaLista = ""; 
      }
    }
  };
</script>

<style scoped>
input, button {
  padding: 5px;
}
input {
  border: 1.7px solid #4b4b4b;
}
button {
  background-color: #d6e2f5;
  border: 1.7px solid #4b4b4b;
  margin-left: 1px;
  cursor: pointer;
}
ul {
  width: 30%;
  margin: 0 auto;
  text-align: left;
  padding-left: 16em;
}
</style>
