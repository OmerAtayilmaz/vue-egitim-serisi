<template>
  I'M Child
  {{mymessage}}
  <button @click="mymethod()">Hi!</button>
</template>
<script>
// Options api
export default {
  name:"ChildComponent",
  props:["mymessage","mymethod"]
}
</script>
