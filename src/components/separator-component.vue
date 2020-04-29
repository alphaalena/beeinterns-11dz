<template>
  <div class="separator">
     <p>
       <slot/>
     </p>
  </div>
</template>
<script>
export default {
  name: 'separatorComponent'
}
</script>
<style>
  .separator {
    border-bottom: 2px solid #C6C6C5;
  }
</style>
