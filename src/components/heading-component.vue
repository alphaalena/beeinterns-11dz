<template>
  <h1 class="heading">
    <slot/>
  </h1>
</template>
<script>
export default {
  name: 'headingComponent'
}
</script>
<style>
  .heading {
    font-size: 26px;
    color: #000000;
    ;
    }
</style>
