<script setup>
import MyClock from './MyClock.vue'
</script>
<template>
  <div id="app">
    <h1>시계</h1>
    <MyClock></MyClock>
  </div>
</template>
<style scoped>
div#app {
  padding: 0 30px 30px 30px;
  margin: 30px auto;
  max-width: 400px;
  border: 1px solid #ccc;
  box-shadow: 3px 3px 3px #aaa;
}
</style>
