
<template>
  <div style="display: flex; align-items: center;justify-content: center;flex-direction: column;height: 100%">
    <span>Awesome huh? | {{mykey}} | Temam: {{!mytheme?"Light":"Dark"}}</span>
    <button @click="changetheme">{{mytheme?"Light":"Dark"}} Theme</button>
  </div>
</template>
<script>
export default {
  props:["mykey","changetheme","mytheme"]
}
</script>
<style scoped>
span{
  font-size: 32px;
}
button{
  width: 150px;
  height: 40px;
  font-size: 22px;
  background-color: #c9daff;
  border: none;
  border-radius: 12px;
}
</style>
