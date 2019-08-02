<template>
  <div id="donate-page">
    <img src="../../assets/venmo-qr.png"/>
  </div>
</template>

<script>
export default {
  name: 'DonatePage',
  props: {
    url: String,
    height: Number
  }
}
</script>

<style scoped>
  img {
    max-width: 500px;
  }
</style>
