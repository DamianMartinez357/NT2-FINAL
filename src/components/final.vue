
<template>
  <section class="src-components-final">
    <div class = "jumbotron">
      <h1>Conversor a dolares</h1>
    <div>
      Ingrese monto $: <input type="number" v-model="pesos" />
    </div>
    <br>
    <div>
      Valor dolar en $: <input type="number" v-model="cotizacion" />
    </div>
    <br>
    <div>
      <p>Valor convertido USD {{ contarPalabras }}</p>
    </div>

    <hr />
      <table class="table">
        <div class="table-responsive">
          <table class="table table-dark">
            <tr>
              <th>Nro pregunta</th>
              <th>Respuesta</th>
            </tr>
            <tr v-for="(pregunta,index) in preguntas" :key="index" :style="{color: 'black', backgroundColor:'silver'}">
              <td>{{ pregunta.numero }}</td>
              <td>{{ pregunta.respuesta }}</td>
            </tr>
          </table>
        </div>
      </table>
    </div>
    
  </section>
</template>

<script lang="js">


  export default  {
    name: 'src-components-final',
    props: [],
    mounted () {

    },
    data () {
      return {
        pesos: 0,
        cotizacion: 0,
        preguntas : [
                    { numero: 1, respuesta: ['C'] },
                    { numero: 2, respuesta: ['B'] },
                    { numero: 3, respuesta: ['C'] },
                    { numero: 4, respuesta: ['A'] },
                    { numero: 5, respuesta: ['B'] },
                    ]
      
      }
    },
    methods: {

    },
    
    computed: {
    contarPalabras() {
      let conversion = this.pesos / this.cotizacion;
		return conversion
	}
}
}
</script>

<style scoped lang="css"></style>