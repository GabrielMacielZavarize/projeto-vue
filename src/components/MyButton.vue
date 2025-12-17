<template>
  <button @click="$emit('update')">
    {{ title }}
  </button>
</template>

<script>
export default {
  name: 'MyButton',
  props: {
    title:{
      text: String,
      default: '+1'
    }
  }
}
</script>

<style>
button{
  padding: 10px 20px;
  background-color: greenyellow;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 16px;
}
button:hover {
  background-color: green;
}
</style>