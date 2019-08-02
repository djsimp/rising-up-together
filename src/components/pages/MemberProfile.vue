<template>
  <div class="member-profile">
    <img :src="this.img" />
    <div class="name">{{this.name}}</div>
    <div class="title">{{this.title}}</div>
  </div>
</template>

<script>
export default {
  name: 'MemberProfile',
  props: {
    name: String,
    title: String,
    bio: String,
    img: String
  }
}
</script>

<style scoped>
  .member-profile {
    width: 300px;
    box-shadow: 0px 4px 8px -2px rgba(128,128,128,1);
    padding: 15px;
    margin: 20px;
  }
</style>
