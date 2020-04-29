<template>
  <div class="row" :align-items="alignItems" is-active="isActive"><slot/></div>
</template>
<script>
export default {
  name: 'rowComponent',
  props: {
    isActive: Boolean,
    alignItems: Boolean
  }
}
</script>
<style>
  .row {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: 15px;
    align-items: flex-end;
  }
  [align-items] {
    align-items: flex-start;
    justify-content: space-between;
    width: 1100px;
    margin: 0 auto;
  }
</style>
