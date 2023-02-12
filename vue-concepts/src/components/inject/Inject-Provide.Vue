<template>
    <div>
        <h1>Injected Here</h1>
       
       
    </div>
</template>

<script>
import ComponentC from './Component-C.vue';

export default {
    data() {
        return {};
    },
    provide: {
        username: "jomobrain1"
    },
    components: { ComponentC }
};
</script>