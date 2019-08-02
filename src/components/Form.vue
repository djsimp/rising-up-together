<template>
  <div id="form-container">
    <iframe :src="url" width="590" :height="height" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
  </div>
</template>

<script>
export default {
  name: 'Form',
  props: {
    url: String,
    height: Number
  }
}
</script>

<style scoped>
</style>
