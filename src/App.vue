<template>
  <div id="app">
    <header-component/>
<!--    <divider title="BUSINESS MAILING ADDRESS"/>-->
  </div>
</template>

<script>
import headerComponent from './components/header-component.vue'
export default {
  name: 'App',
  components: {
    headerComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Roboto, sans-serif;
}
</style>
