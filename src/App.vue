<template>
<div class="container">
  <Header/>
  <div class="main-part">
    <Main/>
  </div>
</div>

</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
export default {
  name: 'App',
  components: {
    Header,
    Main,
  }
}
</script>

<style lang="scss">
@import "./assets/sass/generics.scss";
</style>
