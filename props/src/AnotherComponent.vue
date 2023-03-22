<template>
  <hr/>
  I'M AnotherChild
  {{mymessage}}
  <button @click="mymethod()">Hi!</button>
</template>
<script setup>
// Composition api
defineProps(["mymessage","mymethod"])
</script>
