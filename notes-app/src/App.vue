<script setup>
import { ref,onMounted } from 'vue';
let notes=ref([])

  

 const showModal=ref(false)
 const newNote=ref("") 
 
 const showErrorMessage=ref("")

//  function getRandomColor() {
//   return   "hsl(" + Math.random() * 360 + ", 100%, 75%)";
// }
function getDarkColor() {
    var color = '#';
    for (var i = 0; i < 6; i++) {
        color += Math.floor(Math.random() * 10);
    }
    return color;
}
 const addNote=()=>{
    if(newNote.value.length<10){
      return  showErrorMessage.value="note must be more than 5 characters"
    }
    notes.value.push({
        id:Math.floor(Math.random()*10000),
        text:newNote.value,
        date:new Date(),
        background:getDarkColor()
    }),
    
   
    showModal.value=false
    newNote.value=""
    showErrorMessage.value=""
 }
</script>

<template>
<main>
    <div v-if="showModal" class="overlay">
        <div  class="modal">
            <textarea v-model.trim="newNote"  class="note" cols="30" rows="8"></textarea> <br>
            <p class="error" v-if="showErrorMessage">{{showErrorMessage}}</p>
            <button class="add" @click="addNote" >add note</button> <br>
            <button @click="showModal=!showModal" class="close">close</button>
        </div>
    </div>
    <section class="app">

        <div class="head">
            <h1>Notes App</h1>
          
             <button @click="showModal=!showModal" class="add-notes">+</button>
        </div>
        <div class="notes">
        <div 
        class="note-card" 
        v-for="note in notes" 
        :key="note.id"
        :style="{background:note.background}"
        >
             <p>{{ note.text }}</p>
             <p class="date">{{note.date.toLocaleString("en-Us")}}</p>    
        </div>
        </div>
    </section>
</main>
</template>


