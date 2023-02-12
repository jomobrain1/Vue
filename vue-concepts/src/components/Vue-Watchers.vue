<template>
    <div>
        <h1>Volume 0-20</h1>
        <h2>Volum Tracker is {{ volume }}</h2>
        <button @click="volume+=4"> increase volume</button>
    </div>
</template>

<script>
export default {
  

    data() {
        return {
          volume:0  
        };
    },
  watch:{
     volume(newVal){
        if(newVal>20)
        alert('Loud Music is harmfu')
     }
  }
   
};
</script>

