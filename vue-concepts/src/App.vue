<script setup>
import ParentGreet from "./components/props/Parent-Greet.vue"
import VueBind from './components/Vue-Bind.vue'
import VueConditions from './components/Vue-Conditions.vue';
import VueEvents from './components/Vue-Events.vue';
import VueFormHandling from './components/Vue-Form-Handling.vue';
import VueListsRendering from './components/Vue-Lists-Rendering.vue';
import VueMethods from './components/Vue-Methods.vue';
import VueModifiers from './components/Vue-Modifiers.vue';
import VueWatchers from './components/Vue-Watchers.vue';
import InjectProvide from "./components/inject/Inject-Provide.vue"
</script>

<template>
  <div class="container">
   <!-- <VueBind></VueBind> -->
  <!-- <VueConditions></VueConditions> -->
  <!-- <VueListsRendering></VueListsRendering> -->
  <!-- <VueMethods></VueMethods> -->
  <!-- <VueEvents></VueEvents> -->
  <!-- <VueFormHandling></VueFormHandling> -->
  <!-- <VueModifiers></VueModifiers> -->
   <!-- <VueWatchers></VueWatchers> -->
   <!-- Props shown here -->
    <!-- <ParentGreet></ParentGreet> -->

  <!--Provide and Injection -->
  <InjectProvide></InjectProvide>
  </div>

</template>


