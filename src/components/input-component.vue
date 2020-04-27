<template>
  <div>
    <label v-if="label" for="window">{{label}}</label>
    <input class="input" id="window" type="text" :placeholder="placeholder" :right-input="rightInput"/>
    <p v-if="text">{{text}} </p>
  </div>
</template>
<script>
export default {
  name: 'inputComponent',
  props: {
    label: String,
    text: String,
    placeholder: String,
    rightInput: Boolean
  }
}
</script>
<style>
  .input {
    height: 40px;
    width: 100%;
    border: 1px solid #C6C6C5;
    box-sizing: border-box;
    padding-left: 20px;
    border-radius: 5px;
  }
  [right-input] {
    border-bottom-right-radius: 0;
    border-top-right-radius: 0 ;
  }
</style>
