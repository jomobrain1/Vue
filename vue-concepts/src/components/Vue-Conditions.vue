<template>
    <div>
        <h1>Vue Conditions</h1>
        <p v-if="num==5">Num is equal to 5</p>
        <p v-else> Else Statement </p>
        <h2>Using Vue Show</h2>
        <!-- V-show the element just gets applied the style display none -->
        <div v-show="show">This text is seen courtesy of <b>V-Show</b>    </div>
    </div>

</template>

<script>
export default {
  

    data() {
        return {
          num:5 ,
          show:true 
        };
    },

   
};
</script>