<template>
  <h1 class="text-center" >Event Modifiers</h1>
  <ul >
    <li>.stop</li>
    <li>.prevent</li>
    <li>.once</li>
    <li>.capture</li>
    <li>.self</li>
    <li>.passive</li>
  </ul>

  <hr/>
  <h1>.stop</h1>
  <div class="modal-layout" @click="parentElement()">
    <button class="btn btn-primary" @click.stop="closeModal">Click Me!</button>
  </div>

  <hr/>
  <h1>.prevent</h1>
  <form @submit.prevent="parentElement()">
    <input class="form-control" />
    <button class="btn btn-primary" type="submit">Gönder</button>
  </form>

  <hr/>
  <h1>.once</h1>
  <button class="btn btn-warning" @click.once="parentElement">Send E-mail</button>

  <hr/>
  <h1>.self</h1>
  <div class="container p-5 bg-danger" @click.self="parentElement">
    <div class="row">
      <button class="btn btn-info">Click Me!</button>
    </div>
  </div>

  <hr/>
  <h1>.capture</h1>
  <div class="container p-5 bg-dark" @click.capture="parentElement">
    <div class="row">
      <button class="btn btn-outline-primary">Captured!</button>
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
