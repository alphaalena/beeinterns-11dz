<template>
  <header class="header">
    <container-component>
      <slot/>
    </container-component>
  </header>
</template>
<script>
import ContainerComponent from './container-component'
export default {
  name: 'header-component',
  components: { ContainerComponent }
}
</script>
<style>
  .header {
    height: 100px;
    display: flex;
    flex-direction: row;
    align-items: center;
  }
</style>
