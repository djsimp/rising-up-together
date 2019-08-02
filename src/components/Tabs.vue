<template>
  <div id="links">
    <div class="tab" v-for="(link, index) in tabs" :key="index" :class="{ 'active': link === curTab }" @click="tabClicked">
      <Link :label="link" :active="link === curTab"/>
    </div>
  </div>
</template>

<script>
import Link from './Link.vue'
export default {
  name: 'Tabs',
  props: {
    tabs: Array,
    curTab: String
  },
  components: {
    Link
  },
  methods: {
    tabClicked: function(event) {
      var target = event.target.classList.contains("tab") ? event.target : event.target.closest(".tab");
      if(!target.classList.contains("active")) {
        this.$emit('tab-clicked', target.innerText);
      }
      // var activeTabEls = document.getElementsByClassName("active");
      // for(var i = 0; i < activeTabEls.length; i++) {
      //   activeTabEls[i].classList.remove("active");
      // }
      // target.classList.add("active");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #links {
    display: flex;
    flex-wrap: wrap;
  /*  height: 100%; */
    min-width: 75%;
    justify-content: center;
  }
  .tab {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-grow: 1;
    height: 50px;
    padding: 0px 10px;
  }
  .tab:hover, .active {
    color: #2c3e50;
  }
  .tab:hover {
    background-color: rgba(255,255,255,.5);
    cursor: pointer;
  }
  .active, .active:hover {
    background-color: rgba(255,255,255,.7);
  }
</style>
