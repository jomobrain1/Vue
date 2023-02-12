<template>
    <div>
        <h1>Parent Greet</h1>
        <!-- <Greet name="jomobrain1" role="frontend"> </Greet>
        <Greet :name="name" :role="school"></Greet> -->
        <Article 
        title="The first title is here"
        :likes="50"
        :published="true"
        id="my-article"
        ></Article>
    </div>
</template>

<script>
import Greet from './Greet.vue';
import Article from './Article.vue';
export default {
    data() {
        return {
            name:'beast402',
            school:"jsbits"
        };
    },
    components: { Greet,Article }
};
</script>