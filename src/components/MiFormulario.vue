<template>

<div class="row">
  <div class="col s2"></div>
  <div class="col s8">
    <h3>Arma tus juguetes personalizados</h3>
      <div class="card card-panel left-align">
        <div class="card-image">
          <img src="https://www.compassselfstorage.com/wp-content/uploads/2019/09/vintage-toys.jpg">
        </div>
        <div class="card-content">
          <form action="" class="align-left">
            <h5>Tu nombre</h5>
            <p>
            <input type="text" v-model="nombre">
            </p>
          
            <h5>Tipo de juguete:</h5>
            <p>
              <select v-model="tipo_juguete" class="input-field">
                <option value="bloques">Bloques</option>
                <option value="autos">Autos</option>
                <option value="peluche">Peluche</option>
                <option value="pelotas">Pelotas</option>
              </select>  
            </p>

            <h5>Lugar para jugar:</h5>
            <p>
              <select v-model="categoria_lugar" >
                <option value="casa">Casa</option>
                <option value="departamento">Departamento</option>
                <option value="patio">Patio</option>
                <option value="playa">Playa</option>
                <option value="nieve">Nieve</option>
              </select>  
            </p>

            <h5>Escoge un o más colores:</h5>
            <p>
              <label>
                <input type="checkbox" value="azul" v-model="checkedColores" />
                <span>Azul</span>
              </label>
            </p>
            <p>
              <label>
                <input type="checkbox" value="rojo" v-model="checkedColores" />
                <span>Rojo</span>
              </label>
            </p>

            <p>
              <label>
                <input type="checkbox" value="verde" v-model="checkedColores" />
                <span>Verde</span>
              </label>
            </p>
            <p>
              <label>
                <input type="checkbox" value="amarillo" v-model="checkedColores" />
                <span>Amarillo</span>
              </label>
            </p>
            <p>
              <label>
                <input type="checkbox" value="rosado" v-model="checkedColores" />
                <span>Rosado</span>
              </label>
            </p>
            <p>
              <label>
                <input type="checkbox" value="morado" v-model="checkedColores" />
                <span>Morado</span>
              </label>
            </p>

            <h5 left>Materialidades favoritas:</h5>
            <p>
              <label>
                <input name="group1" type="radio" value="madera" v-model="radioMateriales" />
                <span>Madera</span>
              </label>
            </p>
            <p>
              <label>
                <input name="group1" type="radio" value="plastico" v-model="radioMateriales" />
                <span>Plástico</span>
              </label>
            </p>
            <p>
              <label>
                <input name="group1" type="radio" value="tela" v-model="radioMateriales" />
                <span>Tela</span>
              </label>
            </p>
            <p>
              <label>
                <input name="group1" type="radio" value="espuma" v-model="radioMateriales" />
                <span>Espuma</span>
              </label>
            </p>
            <br>
            <h6>Si necesitas agregar algo más puedes dejarnos un mensaje</h6>
            <textarea id="mensaje" class="materialize-textarea" v-model="mensaje"></textarea>
            <label for="textarea1"></label>
          </form>
          <div>
            <button class="btn waves-effect waves-light" type="submit" name="action" @click="submit">Enviar</button>
          </div>
      </div>
    </div>
  </div>
  <div class="col s2"></div>
</div>
</template>

<script>
import M from 'materialize-css'
export default {
  name: 'MiFormulario',
  data: function() {
    return {
      nombre: '',
      tipo_juguete: '',
      categoria_lugar:'',
      checkedColores: [],
      radioMateriales: [],
      mensaje: ''
    }
  },
  mounted: function() {
    var elems = document.querySelectorAll('select');
    M.FormSelect.init(elems, {});
  },
  methods: {
    submit: function(ev){
      ev.preventDefault();
      alert( 'TUS PREFENRENCIAS SON: ' + ' NOMBRE: ' + this.nombre + ' TIPO DE JUGUETE: ' + this.tipo_juguete + ' LUGAR: ' + this.categoria_lugar + ' COLORES: ' + this.checkedColores + ' MATERIALES: ' + this.radioMateriales + ' MENSAJE: ' + this.mensaje)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>