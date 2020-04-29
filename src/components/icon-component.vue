<template>
  <img  class="icon" :src="'/' + iconName + '.png'">
</template>
<script>
export default {
  name: 'iconComponent',
  props: {
    iconName: {
      required: true,
      type: String
    }

  }
}
</script>
<style scoped>
  .icon {
    margin-right: 13px;
  }
</style>
