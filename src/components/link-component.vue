<template>
  <a  class="link" href="#"><p><slot/></p></a>
</template>
<script>
export default {
  name: 'linkComponent'
}
</script>
<style>
.link {
  text-decoration: none;
  color: #737270;
  padding-left: 50px;
}
</style>
