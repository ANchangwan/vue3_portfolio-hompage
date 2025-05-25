<script setup>
import {onMounted, ref,watch} from "vue";
import ChildComp from "./components/ChildComp.vue";

  let count = ref(0);
  let title = "Hello Vue!";
  let color = ref('green');
  let flag = ref(false);

  onMounted(() =>{
    console.log('mounted');
  })
  const increaseCount = () =>{
    count.value++;
  }
  const flagFn = () =>{
    color.value = flag.value ? "green" : "red";
  }

  watch(color, () =>{
    flag.value= !flag.value;
  });
// watch - state 변화를 감지

</script>

<template>
  <div>
    <h1>{{title}}</h1>
    <button @click="count++">Click up</button>
    <span>{{count}}</span>
    <ChildComp :color="color" />
    <button @click="flagFn">chang color</button>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
