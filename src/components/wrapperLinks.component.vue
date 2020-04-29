<template>
  <div class="wrapper">
    <slot/>
  </div>
</template>
<script>
export default {
  name: 'wrapperLinksComponent'
}
</script>
<style>
  .wrapper {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
</style>
