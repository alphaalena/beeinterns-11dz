<template>
  <div class="container"><slot/></div>
</template>
<script>
export default {
  name: 'containerComponent'
}
</script>
<style>
  .container {
    width: 1300px;
    margin: 0 auto;
    display: flex;
    align-items: center;
  }
</style>
