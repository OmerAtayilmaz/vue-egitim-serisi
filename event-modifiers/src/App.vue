<template>
  Event Modifiers
  <h1>.stop</h1>
  <div class="modal-layout" @click="parentElement()">
    <button class="btn btn-primary" @click.stop="closeModal()">Close Modal</button>
  </div>
  <hr/>
  <h1>.prevent</h1>
  <form @submit.prevent="parentElement">
    <input class="form-control" />
    <button class="btn btn-warning" type="submit">Send Me</button>
  </form>
  <hr/>
  <h1>.once</h1>
  <button class="btn btn-warning" @click.once="closeModal">Click Me Once</button>
  <hr/>

  <div class="container" @click.capture="parentElement">
    <h1>.capture</h1>
    <div class="row">
      <button class="btn btn-info" >HELLO WORLD!</button>
    </div>
  </div>
</template>
<script>
export default {
  methods:{
      parentElement() {
        console.log("Div clicked");
      },
      closeModal() {
          console.log("Button clicked");
      }

  }
}
</script>
