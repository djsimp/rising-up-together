<template>
  <div id="header-container">
    <div id="header">
      <div id="logo-container">
        <img alt="Rising Up Together Logo" src="../assets/rising_up_together_logo.jpg">
        <div class="slogan">Lifting Each Other Out of the R.U.T.</div>
      </div>
      <Tabs :tabs="tabs" :cur-tab="activeTab" @tab-clicked="switchTab" />
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import Tabs from './Tabs.vue'

export default {
  name: 'Header',
  props: {
    activeTab: String
  },
  components: {
    Tabs
  },
  data: function() {
    return {
      currentTab: {},
      tabs: [ "HOME", "ABOUT", "SCHOOLS", "COUNSELORS", "STUDENTS", "SPONSORS", "ORGANIZATIONS", "VOLUNTEERS", "SPEAKERS" ]
    }
  },
  methods: {
    switchTab: function(tab) {
      this.$emit('tab-switched', tab)
    }
  },
  mounted() {
    this.switchTab("HOME");
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#header {
  background-color: #808080;
  display: flex;
  flex-direction: column;
  font-weight: 600;
  color: white;
}
.slogan {
  color: black;
  font-size: xx-large;
}
img {
  width: 30vw;
}
#logo-container {
  background-color: #85BADC;
  padding: 20px;
}
</style>
