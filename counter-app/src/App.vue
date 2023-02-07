<script >
export default{
  data() {
    return {
      count: 0
    };
  },

  methods: {
    addCount(){
       this.count++
    }
  },
}
</script>

<template> 

  <main>
     <h1>Counter Application</h1>
     <h2>{{count}}</h2>
     <button @click="addCount()">increment</button>
     <button @click="count--">decrement</button>
  </main>
</template>

<style scope>
 
</style>


