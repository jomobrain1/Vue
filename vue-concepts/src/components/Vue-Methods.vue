

<template>
    <div>
        Vue Methods
        <h5>Add Num Method</h5>
         <p>The sum is {{ addNum(10,14) }}</p>
         <h6>Multiply Function</h6>
         <p>{{ multiply(4) }}</p>
    </div>
</template>

<script>
export default {
    

    data() {
        return {
            base:30
        };
    },

   
    methods: {
        addNum(num1,num2){
            return  num1 + num2
        },
        multiply(num){
         return num * this.base
        } 
        
    },
};
</script>

<style scoped>

</style>