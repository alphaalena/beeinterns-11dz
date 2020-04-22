<template>
  <div id="app">
    <header-component>
      <logo/>
      <input-component placeholder="Search for Products"/>
    </header-component>
    <!--    <divider title="BUSINESS MAILING ADDRESS"/>-->
  </div>
</template>

<script>
import headerComponent from './components/header-component.vue'
import Logo from './components/logo'
import InputComponent from './components/input-component'

export default {
  name: 'App',
  components: {
    InputComponent,
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
