<template>
  <div id="footer">
    <div>
      <font-awesome-icon icon="phone-alt"></font-awesome-icon>
      <span>(801) 425-1212</span>
    </div>
    <div>
      <font-awesome-icon icon="envelope"></font-awesome-icon>
      <span>risinguptogether4hope@gmail.com</span>
    </div>
    <div>
      <span>All Rights Reserved</span>
      <font-awesome-icon icon="trademark"></font-awesome-icon>
    </div>
  </div>
</template>

<script>
//import DevJockey from "./DevJockey.vue"

export default {
  name: 'Footer',
  components: {
  //  DevJockey
  }
}
</script>

<style scoped>
  #footer {
    height: 100px;
    display: flex;
    align-items: center;
    background-color: #85BADC;
    flex-wrap: wrap;
    justify-content: space-around;
    color: white;
    margin-top: 20px;
  }
  span {
    padding: 10px;
  }
</style>
