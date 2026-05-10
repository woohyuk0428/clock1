<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import moment from "moment";

const { format = "HH:mm:ss", interval = 1000 } = defineProps(["format", "interval"]);
const time = ref(null);
const timerId = ref(0);

function start() {
  const callback = () => {
    time.value = moment().format(format);
    console.log(time.value);
  };
  callback();
  timerId.value = setInterval(callback, interval);
}

function stop() {
  clearInterval(timerId.value);
  timerId.value = 0;
}

onMounted( () => {  start() });
onBeforeUnmount( () =>{ stop() });
</script>
<template>
  <div>
    <span>{{ time }}</span>
  <input type="button" @click="start" v-if="timerId == 0" value="start">
  <input type="button" @click="stop" v-if="timerId != 0" value="stop">
  </div>
</template>
<style scoped>
div {
  display: inline-block;
  font-size: 20pt;
  padding: 3px 12px;
  border: 1px solid gray;
}
button { margin-left: 4px; }
</style>
