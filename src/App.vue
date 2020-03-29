<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import Vue from 'vue';

export default Vue.extend({
  name: 'app',
  components: {
    HelloWorld
  }
})
</script>

<style>
</style>
