<template>
  <div id="app">
    <header-component>
      <logo/>
      <input-component placeholder="Search for Products"/>
      <button-component left-flat type="filled">Search</button-component>
    </header-component>
    <!--    <divider title="BUSINESS MAILING ADDRESS"/>-->
  </div>
</template>

<script>
import headerComponent from './components/header-component.vue'
import Logo from './components/logo'
import InputComponent from './components/input-component'
import ButtonComponent from './components/button-component'

export default {
  name: 'App',
  components: {
    ButtonComponent,
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
