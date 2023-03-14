<template>
  <!--HEADER--->
  <div class="container-fluid d-flex justify-content-between  flex-column h-100 m-0 p-0">
    <header>
      <header-component/>
    </header>
    <!--MAIN--->
    <main>
      ABOUT PAGE
    </main>
    <!--FOOTER--->
    <footer>
      <footer-component/>
    </footer>
  </div>
</template>
<script>
import HeaderComponent from "@/common/HeaderComponent.vue";
import FooterComponent from "@/common/FooterComponent.vue";
export default {
  components:{
    HeaderComponent,
    FooterComponent
  }
}
</script>
