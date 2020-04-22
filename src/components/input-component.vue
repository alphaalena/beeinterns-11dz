<template>
  <div>
    <label v-if="label" for="window">{{label}}</label>
    <input class="input" id="window" type="text" :placeholder="placeholder"/>
    <p v-if="text">{{text}} </p>
  </div>
</template>
<script>
export default {
  name: 'inputComponent',
  props: {
    label: String,
    text: String,
    placeholder: String
  }

}
</script>
<style>
  .input {
    height: 40px;
    width: 100%;
    border: 1px solid #C6C6C5;
    box-sizing: border-box;
  }
</style>
