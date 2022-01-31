<template>
  <div id="app">
    <Header />
    <Main />    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main
  }
}
</script>

<style lang="scss">
@import "./assets/my_scss/global.scss";
@import "./assets/my_scss/partials/variables.scss";

body{
  background-color: $mainColor;
}

</style>
