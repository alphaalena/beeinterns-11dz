<template>
  <div id="app">
    <header-component>
      <logo class="margin-right-big"/>
      <input-component class="width-input" placeholder="Search for Products"/>
      <button-component class="margin-right-big" left-flat type="filled">Search</button-component>
      <button-component class="margin-right-little" type="outline">Log in</button-component>
      <button-component class="margin-right-little" type="outline">Sign up</button-component>
      <icon-component class="margin-right-little" icon-name="shortlist icon"/>
      <icon-component icon-name="Cart icon"/>
    </header-component>
    <!--    <divider title="BUSINESS MAILING ADDRESS"/>-->
  </div>
</template>

<script>
import headerComponent from './components/header-component.vue'
import Logo from './components/logo'
import InputComponent from './components/input-component'
import ButtonComponent from './components/button-component'
import IconComponent from './components/icon-component'

export default {
  name: 'App',
  components: {
    IconComponent,
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
