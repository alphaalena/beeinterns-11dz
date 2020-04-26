<template>
  <section class="section-link">
    <container-component>
      <slot/>
    </container-component>
  </section>
</template>
<script>
import ContainerComponent from './container-component'
export default {
  name: 'navigationComponent',
  components: { ContainerComponent }
}
</script>
<style>
  .section-link {
    height: 45px;
    display: flex;
    flex-direction: row;
    align-items: center;
    background: #F4F4F4;
  }
</style>
