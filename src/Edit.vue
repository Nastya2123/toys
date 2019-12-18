<template>
<div>
     <label> Назва<input v-model="newToy.surname"></label>
      <label>Вік <input v-model="newToy.age"></label>
      <label>Ціна <input v-model="newToy.price"></label>
      <button v-on:click="editElement(newToy)"> Додати іграшку</button>
      </div>
</template>
<script>
export default {
     data() {
    return {
        hide:true,
        newToys:this.toys
      }
    },
    props:{
    toys:Array,
    newToy:Object
     },
    methods:{
      addElement:function(value){
      let copy = Object.assign({}, value);   
      this.newToys.push(copy);
    }
    }
}
</script>
<style scoped>

</style>