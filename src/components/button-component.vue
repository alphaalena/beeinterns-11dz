<template>
  <button class="button" :class="type" :left-flat="leftFlat" :is-active="isActive">
    <slot/>
  </button>
</template>
<script>
export default {
  name: 'buttonComponent',
  props: {
    type: {
      type: String,
      default: 'outline'
    },
    leftFlat: Boolean,
    isActive: Boolean
  }
}

// outline
// filled
// flat
</script>
<style>
  .button {
    border-radius: 5px;
    border: none;
    outline: none;
    height:40px ;
    padding-left: 14px;
    padding-right: 14px;
    font-style: normal;
    font-size: 14px;
    line-height: 17px;
  }
  [left-flat] {
    border-bottom-left-radius: 0;
    border-top-left-radius: 0 ;
  }
  .filled {
    background: #007AFF;
    color: #FFFFFF;;
  }
  .outline {
    background-color: transparent;
    border: 1px solid #C6C6C5;
    color: #757575;;
  }
  .flat {
    background-color: transparent;
    color: #757575;;
  }
  [is-active].flat{
    color: #007AFF;
  }
</style>
