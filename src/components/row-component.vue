<template>
  <div class="row"><slot/></div>
</template>
<script>
export default {
  name: 'rowComponent'
}
</script>
<style>
  .row {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    margin-top: 15px;
    align-items: flex-end;
  }
</style>
