<template>

     <table>
        <tr>
          <th> #</th>
          <th>Назва</th>
          <th>Вік</th>
          <th>Ціна</th>
        </tr>
        <tr v-for="(toy, index) in toys" v-bind:key="toy.surname">
            <td> {{index+1}}</td>
            <td> {{toy.surname}}</td>
            <td> {{toy.age}}</td>
            <td> {{toy.price}}</td>
            <td> <button v-on:click="deleteElement(index)">Видалити</button></td>    
           <td><button v-on:click="editElement(newToy)"> Редагувати  </button></td>  
      <tr/>
      
   </table>
 
</template>
 
         </tr>
      </table>
</template>
<script>
export default {
  name: 'app',
  data() {
    return {
        hide:true,
        //newParticipant:{surname:"",age:0,specialty:"",mark1:0,mark2:0,mark3:0},
        //participants: [{surname:"Боднар",age:19,specialty:"Філологічний",mark1:9,mark2:10,mark3:7},{surname:"Кудасова",age:20,specialty:"Біологічний",mark1:0,mark2:6,mark3:10}]
    }
},
props:{
    toys:Array
},
methods:{
   
    addElement:function(){
      this.bool = true;
    },

    deleteElement: function(index){
      this.toys.splice(index,1);
    },
    editElement:function(index){
      let copy = Object.assign({}, index);   
      this.toys.push(copy);
    },
    
    },
    
      
    }

   
</script>
<style scoped>
 table td{
    border: 1px solid black;
    border-collapse: collapse;
    width: 100px;
  }
</style>