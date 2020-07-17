<template>
  <div id="app" class="container blue-grey lighten-5">
    <MiFormulario/>
  </div>
</template>

<script>
import MiFormulario from './components/MiFormulario.vue'

export default {
  name: 'App',
  components: {
    MiFormulario
  }
}
        
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
