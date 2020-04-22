<template>
  <header class="header">
    <div class="container">
      <slot/>
    </div>
  </header>
</template>
<script>
export default {
  name: 'header-component'
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
