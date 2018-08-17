<template>
  <div id="app">   
    <dashboard></dashboard>
  </div>
</template>

<script>

import Dashboard from '../src/components/Dashboard.vue';

export default {
  name: 'app',
  components: {
   Dashboard
  }
}
</script>

<style>
#app {  
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
