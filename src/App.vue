<script setup>
import MyClock from './MyClock.vue'
</script>
<template>
  <div id="app">
    <h1>시계</h1>
    <MyClock id="clock1" class="myClock" />
    <MyClock id="clock2" class="myClock" interval="3000"/>
    <MyClock id="clock3" class="myClock" interval="6000" format="yyyy-MM-DD HH:mm"/>
  </div>
</template>
<style scoped>
div#app {
  padding: 0 30px 30px 30px;
  margin: 30px auto;
  max-width: 600px;
  border: 1px solid #ccc;
  box-shadow: 3px 3px 3px #aaa;
}

.myClock { margin-right: 5px;}
#clock1 { background-color: #ffd; }
#clock2 { background-color: #dfd; font-size: 15pt; }
#clock3 { background-color: #dff; font-size: 12pt; }
</style>
