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
    <p>Colores preferidos:<br>
      <input type="checkbox" value="azul" v-model="checkedColores">
      <label for="azul">Azul</label><br>
      <input type="checkbox" value="verde" v-model="checkedColores">
      <label for="">Verde</label><br>
      <input type="checkbox" value="amarillo" v-model="checkedColores">
      <label for="amarillo">Amarillo</label><br>
      <input type="checkbox" value="rojo" v-model="checkedColores">
      <label for="rojo">Rojo</label><br>
      <br>
       <!--<span>Colores elegidos: {{ checkedColores }}</span>-->
    </p>
    <p>Materialidades favoritas:<br>
      <input type="radio" value="madera" v-model="checkedMateriales">
      <label for="madera">Madera</label><br>
      <input type="radio" value="plastico" v-model="checkedMateriales">
      <label for="plastico">Plástico</label><br>
      <input type="radio" value="tela" v-model="checkedMateriales">
      <label for="tela">Tela</label><br>
      <input type="radio" value="espuma" v-model="checkedMateriales">
      <label for="tela">Espuma</label><br>
      <br>
      <!--<span>Material escogido: {{ checkedMateriales }}</span>-->
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
      checkedColores: [],
      checkedMateriales: []
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
