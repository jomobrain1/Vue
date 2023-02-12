<template>
    <div>
        <h1>Vue Bind</h1>
        <hr> <br>
        <p>bind {{ name }} {{ js }}</p>
        <h2>V-text --text binding</h2>   <br>      
        <p v-text="school"></p>
        <p v-text="js"></p>
        <h2>Using V-html</h2>
         <p v-html="js"></p>
         <hr>
        <h1>Binding Attributes</h1>
        <p v-bind:class="class">The  class  has been binded</p>

        <h2>Bind Classes With If statements</h2>
        <p v-bind:class="isBinded && 'bind'">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Culpa impedit perspiciatis eaque, recusandae autem voluptate sapiente quod ex, optio, porro ducimus. Ab sunt nostrum quo, facilis vero corporis fugit ut.
        </p>
        <h3>Binded with Ternary Operator</h3>
          <p v-bind:class="isSold ? 'sold' :'notsold' ">Is Sold</p>
          <hr>
          <h2>Binding Multiple Classes</h2>
          <p :class="['underline','background']" >
             Laborum dolore delectus accusantium atque dignissimos quam illum fuga provident ea. Nesciunt quod exercitationem rerum quasi modi magni.
          </p>
        <hr>
        <!--How to Bind Styles  -->
        <h2>Binding Styles</h2>
        <p :style="
           {
            color:'red',
            fontSize:myfontSize
           
           }">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Modi in non id natus est rerum a dignissimos odio consequuntur tempore, velit quod illum iusto aliquam quidem possimus, fuga quasi aspernatur?
        </p>
        

    </div>
</template>

<script>
export default {
    data() {
        return {
            name:"jomo brain",
            school:"jsbits",
            js:"<b>jscode</b>",
            class:"binded-para",
            isBinded:true,
            isSold:true,
            myfontSize:"26px"
        };
    },

};
</script>
<style>
.binded-para{
    background: blue;
    height: 6.25rem;
    color: #fff;
    display: grid;
    place-content: center;
}
.bind{
    color: steelblue;
    font-weight: 800;
}
.sold{
    font-size: large;
    color: green;
}
.notsold{
    color: red;
}
.background{
    background: orangered;
    height: 90px;
}
.underline{
    text-decoration: underline;
    color: #fff;
}
</style>