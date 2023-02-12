<template>
    <div>
        <h1>Vue Events</h1> <hr> <br> <br> 
        <p>{{ name }}</p> <h4>{{ count }}</h4>
        <button @click="changeName($event), increment(3,$event)">change Name</button>
    </div>
</template>

<script>
export default {
    name: 'VueConceptsVueEvents',

    data() {
        return {
            name:"jomobrain1",
            count:0
        };
    },

    
    methods: {
         changeName(e){
             console.log(e);
             this.name="beast402"
         },
         increment(num){
              this.count+=num
         }
    },
};
</script>

<style scoped>
h3:hover{
    cursor: pointer;
}
</style>