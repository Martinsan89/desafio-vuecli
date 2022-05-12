<template>
  <div id="app">
     <DesafioTablas
        :titulos="tabla1.titulos"
        :registros="tabla1.registros"
        :clases="tabla1.clases"
        :indice="tabla1.indice"
      />
      <DesafioTablas
        :titulos="tabla2.titulos2"
        :registros="tabla2.registros2"
        :clases="tabla2.clases2"
        :indice="tabla2.indice2"
      />
      <DesafioTablas
        :titulos="tabla3.titulos3"
        :registros="tabla3.registros3"
        :clases="tabla3.clases3"
        :indice="tabla3.indice3"
      />
  </div>
</template>

<script>
import DesafioTablas from './components/DesafioTablas.vue'

export default {
  name: 'App',
  components: {
    DesafioTablas
  },
  data(){
     return{
        tabla1: {
                titulos: ["ID", "Nombre", "Apellido", "Provincia"],
                registros: [
                    ["Jose", "Velez", "San Luis"],
                    ["Ramon", "Gomez", "Santa Fe"],
                    ["Marcelo", "Godino", "Buenos Aires"],
                    ["Ramiro", "Gimenez", "Salta"],
                ],
                clases: {
                    "table-dark": true,
                    "text-secondary": true,
                },
                indice: {
                    "background-color": "cadetblue",
                    "color": "black",
                },
        },
        tabla2: {
            titulos2: ["ID", "Nombre", "Apellido", "Provincia"],
            registros2: [
                ["Celso", "Fernandez", "La Pampa"],
                ["Matias", "Perez", "Formosa"],
                ["Marcela", "Garcia", "Chaco"],
                ["Omar", "Ramirez", "Misiones"],
            ],
            clases2: {
                "table-info": true,
                "text-success": true,
            },
            indice2: {
                "background-color": "black",
                "color": "white",
            },
        },
        tabla3: {
            titulos3: ["ID", "Nombre", "Apellido", "Provincia"],
            registros3: [
                ["Ernesta", "Resta", "Chubut"],
                ["Joaquin", "Morales", "Rio Negro"],
                ["Roberto", "Sanchez", "Tucuman"],
                ["Debora", "Esquer", "Tierra del fuego"],
            ],
            clases3: {
                "table-danger": true,
                "text-primary": true,
            },
            indice3: {
                "background-color": "brown",
                "color": "white",
            },
        }
      }
  } 
}
</script>

<style scoped>
#app {

 width: 80%;
 margin: 1rem auto;
}
</style>
