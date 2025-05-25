<script setup>
const props = defineProps({
  color:String,
  bgColor:String,
})
console.log(props.color  )

</script>

<template>
  <div>
    <h2>ChildComp</h2>
    <span :style="{color, backgroundColor: bgColor}">{{color}}</span>
  </div>
</template>

<style scoped>

</style>