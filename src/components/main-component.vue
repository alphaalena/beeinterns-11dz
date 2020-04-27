<template>
  <main class="main">
    <container-component>
      <slot/>
    </container-component>
  </main>
</template>
<script>
import ContainerComponent from './container-component'
export default {
  name: 'mainComponent',
  components: { ContainerComponent }
}
</script>
<style>
</style>
