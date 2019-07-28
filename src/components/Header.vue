<template>
  <div id="header-container">
    <div id="header">
      <img alt="Vue logo" src="../assets/rising_up_together_logo.jpg">
      <Tabs :tabs="tabs" :cur-tab="activeTab" @tab-clicked="switchTab" />
    </div>
    <div id="border">
      <div>Lifting each other out of the R.U.T.</div>
    </div>
  </div>
</template>

<script>
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
      tabs: [
        {
          label: "ABOUT",
          active: false,
          url: "/about"
        }, /*{
          label: "CONTACT US",
          active: false,
          url: "/contact-us"
        }, */{
          label: "SPEAKERS",
          active: false,
          url: "/speakers"
        }, {
          label: "VOLUNTEERS",
          active: false,
          url: "/volunteers"
        }, {
          label: "DONATE",
          active: false,
          url: "/speakers"
        }, /*{
          label: "SCHOOL DISTRICT",
          active: false,
          url: "/school-district"
        }, {
          label: "COMMUNITY ORGANIZATIONS",
          active: false,
          url: "/community-organizations"
        }, {
          label: "SPONSORS",
          active: false,
          url: "/sponsors"
        }, {
          label: "DONATE NOW",
          active: false,
          url: "/donate-now"
        }, {
          label: "COUNSELORS",
          active: false,
          url: "/counselors"
        }, {
          label: "STUDENTS",
          active: false,
          url: "/students"
        }*/
      ]
    }
  },
  methods: {
    switchTab: function(tab) {
      for(var i = 0; i < this.tabs.length; i++) {
        this.tabs[i].active = false;
        if(this.tabs[i].label === tab) {
          var temp = this.tabs[i];
          temp.active = true;
          this.tabs.splice(i, 1, temp);
          this.$emit('tab-switched', tab)
        }
      }
    },
  },
  mounted() {
    this.switchTab("ABOUT");
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#header-container {
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
}
#header {
  background-color: grey;
  display: flex;
  justify-content: space-between;
  font-size: small;
  font-weight: 600;
  color: white;
}
img {
  height: 80px;
  margin: 10px;
}
#border {
  background-color: black;
  color: white;
  padding: 5px 10px;
  font-weight: 500;
  display: flex;
}
</style>
