<template>
  <img :src="'/' + iconName + '.png'">

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
<style>
</style>
