<template>
  <form action="">
    <h3>Juguetes</h3>
    <p>Tu nombre: <input type="text" v-model="nombre"></p>
    <p>Categoría de juguete:
      <select v-model="categoria_juguete" >
        <option value="bloques">Bloques</option>
        <option value="autos">Autos</option>
        <option value="peluche">Peluche</option>
        <option value="pelotas">Pelotas</option>
      </select>  
    </p>
    <p>Lugar para jugar:
      <select v-model="categoria_lugar" >
        <option value="dormitorio">Dormitorio</option>
        <option value="patio">Patio</option>
        <option value="playa">Playa</option>
      </select>  
    </p>
    <p>Materialidades favoritas:<br>
      <input type="checkbox" id="madera" value="madera" v-model="checkedNames">
      <label for="madera">Madera</label><br>
      <input type="checkbox" id="plastico" value="plastico" v-model="checkedNames">
      <label for="plastico">Plastico</label><br>
      <input type="checkbox" id="tela" value="tela" v-model="checkedNames">
      <label for="tela">Tela</label><br>
      <br>
      <span>Checked names: {{ checkedNames }}</span>
    </p>
  </form>
</template>

<script>
export default {
  name: 'MiFormulario',
  data: function() {
    return {
      nombre: '',
      categoria_jueguete: '',
      categoria_lugar:'',
      checkedNames: []
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
