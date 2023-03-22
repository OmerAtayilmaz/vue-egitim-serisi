<template>
  <child-component :mymessage="message" :mymethod="printMessage"/>
  <another-component :mymessage="message" :mymethod="printMessage"/>
</template>
<script>
import ChildComponent from "./ChildComponent.vue";
import AnotherComponent from "./AnotherComponent.vue";
export default {
  components:{
    ChildComponent,
    AnotherComponent
  },
  data:function (){
    return {
      message: "Lorem ipsum"
    }
  },
  methods:{
    printMessage(){
      alert("Are u sure?");
    }
  }
}
</script>
