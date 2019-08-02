<template>
  <div class="profile-container">
    <div class="grey-background" v-if="this.isActive" @click="toggleProfile"></div>
    <div class="member-profile" :class="{ 'active': this.isActive }" @click="toggleProfile">
      <div class="image-container">
        <img v-if="name === 'Shelly A. Jordan'" src="../../assets/board-members/Shelly-Jordan.jpg" />
        <!--<img v-if="name === 'Elise Cole'" src="../../assets/board-members/Elise-Cole.JPG" />-->
        <!--<img v-if="name === 'Jill Laurence'" src="../../assets/board-members/Jill-Laurence.JPG" />-->
        <img v-if="name === 'Ashley Garbe Smith'" src="../../assets/board-members/Ashley-Garbe-Smith.jpg" />
        <img v-if="name === 'Brady Griffin'" src="../../assets/board-members/Brady-Griffin.jpg" />
        <img v-if="name === 'Lorene Lillywhite'" src="../../assets/board-members/Lorene-Lillywhite.jpg" />
        <img v-if="name === 'Lauren Miner Zufelt'" src="../../assets/board-members/Lauren-Miner-Zufelt.jpg" />
        <img v-if="name === 'Kristianne Rushton'" src="../../assets/board-members/Kristianne-Rushton.jpg" />
      </div>
      <div class="name">{{this.name}}</div>
      <div class="title">{{this.title}}</div>
      <div class="bio">
        <p v-for="(paragraph, index) in bio" :key="index">{{paragraph}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MemberProfile',
  props: {
    name: String,
    title: String,
    bio: Array,
    img: String
  },
  data: function() {
    return {
      url: this.img,
      isActive: false
    }
  },
  methods: {
    toggleProfile:  function() {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style scoped>
  .image-container {
    width: 240px;
    height: 240px;
    min-height: 240px;
    overflow: hidden;
    border-radius: 50%;
  }
  .name, .title {
    font-size: large;
    font-weight: 600;
    margin: 10px;
  }
  .member-profile {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 300px;
    box-shadow: 0px 4px 8px -2px rgba(128,128,128,1);
    padding: 15px;
    margin: 20px;
  }
  .member-profile img {
    width: 240px;
  }
  .bio {
    display: none;
  }
  .grey-background {
    z-index: 5;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(50,50,50,.5);
  }
  .active {
    width: 50%;
    position: absolute;
    top: 600px;
    left: 0;
    right: 0;
    margin: auto;
    z-index: 10;
    background-color: white;
  }
  .active .bio {
    display: block;
  }
</style>
