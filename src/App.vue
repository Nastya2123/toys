<template>
  <div id="app">
     <ToyTable v-bind:toys="toys"></ToyTable>
     <Add v-bind:newToy="newToy" v-bind:toys="toys"></Add>
     </div>
</template>

<script>
import ToyTable from "./ParticipantTable.vue"
import Add from "./Add.vue"
export default {
  methods:{
   
    
  },
  components:{
    ToyTable,Add},

   data() {
    return {
        hide:true,
        newToy:{surname:"",age:0,price:0},
        toys: [{surname:"Барбі",age:10,price:1200},{surname:"Лего",age:18,price:1600}]
    }
}
}
</script>

<style scoped>
  table td{
    border: 1px solid black;
    border-collapse: collapse;
    width: 100px;
  }
</style>