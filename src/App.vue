<template>
  <div id="app">
    <header-component>
      <logo/>
    </header-component>
    <!--    <divider title="BUSINESS MAILING ADDRESS"/>-->
  </div>
</template>

<script>
import headerComponent from './components/header-component.vue'
import Logo from './components/logo'

export default {
  name: 'App',
  components: {
    Logo,
    headerComponent
  }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Roboto, sans-serif;
  }
</style>
