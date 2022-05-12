<template>
  <div>
    <table class="table" :class="clases">
        <thead  >
            <tr>
                <th :style="indice" v-for="(item, i) in titulos" :key="i" scope="col">{{ item }}</th>
            </tr>
        </thead>
        <tbody>
             <tr v-for="(registro, i) in registros" :key="i">
               <th>{{ i + 1 }}</th>
                <th v-for="(row, r) in registro" :key="r">{{row}}</th>
              </tr>
         </tbody>
    </table>
  </div>
</template>

<script>
export default {
    props: {
        titulos: {
        type: Array,
        required: true,
        },
        registros: {
        type: Array,
        required: true
        },
        clases: {
        type: Object,
        required: true
        },
        indice: {
        type: Object,
        required: true
        }
    },
}
</script>

