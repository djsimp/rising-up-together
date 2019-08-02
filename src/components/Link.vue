<template>
  <div class="link">
    {{ label }}
  </div>
</template>

<script>
export default {
  name: 'Links',
  props: {
    label: String,
    active: Boolean
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .link {
    padding: 5px;
  }
</style>
