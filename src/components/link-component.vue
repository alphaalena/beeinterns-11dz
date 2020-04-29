<template>
  <a  class="link" href="#" link-black="linkBlack" is-active="isActive"><p><slot/></p></a>
</template>
<script>
export default {
  name: 'linkComponent',
  props: {
    isActive: Boolean,
    linkBlack: Boolean
  }
}
</script>
<style>
.link {
  text-decoration: none;
  color: #737270;
  margin-right: 40px;
}
  [link-black] {
    color: #1C1C1B;
    padding-top: 10px;
    padding-bottom: 10px;
    font-weight: bold;
  }
</style>
