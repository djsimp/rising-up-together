<template>
  <div id="devjockey-container">
    This website was created by <a href="http://dev-jockey.com">DevJockey Solutions</a>.
  </div>
</template>

<script>
export default {
  name: 'DevJockey',
  props: {
    url: String,
    height: Number
  }
}
</script>

<style scoped>
  #devjockey-container {
    height: 100px;
    width: 100px;
    background-color: black;
    color: white;
  }
</style>
