<template>
  <form class="form">
    <slot/>
  </form>
</template>
<script>
export default {
  name: 'formComponent'
}
</script>
<style>
  .form {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    width: 970px;
    margin: 0 auto;
  }

</style>
