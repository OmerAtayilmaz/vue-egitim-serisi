<template>
  <div :class="!theme?'light':'dark'" style="height: 100vh;">
    <child-component :mykey="message" :mytheme="theme" :changetheme="toggleTheme"/>
  </div>
</template>
<script>
import ChildComponent from "./ChildComponent.vue";
export default {
  components:{
    ChildComponent
  },
  data(){
    return {
      message:"Hello From Parent Component",
      theme:false
    }
  },
  methods:{
    toggleTheme(){
      this.$data.theme = !this.$data.theme;
    }
  }
}
</script>
<style>
.light{
  background-color: #f0f0f9;
  color: #162035;
}
.dark{
  color: #f0f0f9;
  background-color: #162035;
}
</style>
