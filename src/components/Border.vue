<template>
  <div id="border">
    <div class="tab" v-for="link in menu" :key="link" :class="{ 'active': link === activeTab }" @click="tabClicked">
      <Link :label="link" :active="link === activeTab"/>
    </div>
  </div>
</template>

<script>
import Link from './Link.vue'
export default {
  name: 'Border',
  props: {
    activeTab: String,
    menu: Array
  },
  components: {
    Link
  },
  computed: {
  },
  methods: {
    tabClicked: function(event) {
      var target = event.target.classList.contains("tab") ? event.target : event.target.closest(".tab");
      if(!target.classList.contains("active")) {
        this.$emit('sub-tab-clicked', target.innerText);
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
  #border {
    background-color: black;
    height: 32px;
    color: white;
    font-weight: 500;
    display: flex;
  }
  #border-tabs {
    display: flex;
    flex-wrap: wrap;
  /*  height: 100%; */
    min-width: 75%;
    justify-content: center;
  }
  .tab {
    display: flex;
    flex-grow: 1;
    justify-content: center;
    align-items: center;
    height: 100%;
    padding: 0px 10px;
  }
  .tab:hover {
    cursor: pointer;
  }
  .active {
    background-color: white;
    color: black;
  }
</style>
