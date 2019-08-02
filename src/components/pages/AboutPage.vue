<template>
  <div id="page-content">
    <Border :menu="menu" :active-tab="activeTab" @sub-tab-clicked="subTabClicked" />
    <div id="about-page">
      <MissionVision v-if="activeTab === 'Mission & Vision'" />
      <BoardTrustees v-if="activeTab === 'Board of Trustees'" />
    </div>
  </div>
</template>

<script>
import Border from '../Border.vue'
import MissionVision from './MissionVision.vue'
import BoardTrustees from './BoardTrustees.vue'

export default {
  name: 'AboutPage',
  props: {
    url: String,
    height: Number
  },
  components: {
    Border,
    MissionVision,
    BoardTrustees
  },
  data: function() {
    return {
      activeTab: "Mission & Vision",
      menu: [ "Mission & Vision", "Board of Trustees" ]
    }
  },
  methods: {
    subTabClicked: function(tab) {
      this.activeTab = tab;
    }
  }
}
</script>

<style scoped>
  #about-page {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
