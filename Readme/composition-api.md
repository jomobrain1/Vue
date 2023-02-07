
`



<script setup>
import { ref } from 'vue';
const count=ref(0)
</script>

<template> 

  <main>
     <h1>Counter Application</h1>
     <h2>{{count}}</h2>
     <button @click="count++">increment</button>
     <button @click="count--">decrement</button>
  </main>
</template>

<style scope>
 
</style>

















`