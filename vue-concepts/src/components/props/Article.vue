<template>
    <div>
       <h4>Article is Here</h4> 
        <hr>
        <h3 v-bind="$attrs">Title is : {{ title }}</h3>
        <p>Number of Likes: {{ likes }}</p>
        <strong>published? : {{ published?"Yes":"No" }}</strong>
    </div>
</template>

<script>
export default { 
   props:{
    title:{
       type:String,
       required:true,
       default:"This is default and appears if no prop is specified"
    },
    likes:Number,
    published:Boolean

   },
    data() {
        return {
            
        };
    },
inheritAttrs:false
  
};
</script>