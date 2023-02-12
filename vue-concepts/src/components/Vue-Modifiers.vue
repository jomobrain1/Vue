<template>
    <div>
     <h1>Modifiers</h1> 
     <!-- Removes Space before input or after -->
     <h2>Trim Modifier  <i>{{ form.name }}</i> </h2> 
     <input type="text" v-model.trim="form.name"> 
     <h2>Trim and Lazy modifier</h2>
     <input type="text" v-model.trim.lazy="form.name"> 
     
     <h1>Number {{form.age }}</h1>
     <input type="text" v-model.number="form.age">
    </div>
</template>

<script>
export default {
 

    data() {
        return {
          form:{
            name:"jomobrain 1",
            age:null
          }   
        };
    },

    mounted() {
        
    },

    
};
</script>