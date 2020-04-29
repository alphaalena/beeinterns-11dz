<template>
  <div class="separator" :is-active="isActive"  :width-separator="widthSeparator">
     <p>
       <slot/>
     </p>
  </div>
</template>
<script>
export default {
  name: 'separatorComponent',
  props:
    {
      widthSeparator: Boolean,
      isActive: Boolean
    }

}
</script>
<style>
  .separator {
    border-bottom: 2px solid #C6C6C5;
  }
  [width-separator] {
    width: 1300px;
    margin: 0 auto;
    padding-top: 20px;
  }
</style>
