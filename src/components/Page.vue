<template>
  <div id="page-body">
    <Header :active-tab="curPage" @tab-switched="switchPage" />
    <div id="page-content">
      <AboutPage v-if="curPage === 'ABOUT'" />
      <Form v-if="curPage === 'SPEAKERS' || curPage === 'VOLUNTEERS'" :url="formUrl" :height="formHeight" />
      <DonatePage v-if="curPage === 'DONATE'" />
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from "./Header.vue"
import Form from "./Form.vue"
import AboutPage from "./AboutPage.vue"
import DonatePage from "./DonatePage.vue"
import Footer from "./Footer.vue"

export default {
  name: 'Page',
  props: {
    page: String,
  },
  data: function() {
    return {
      curPage: this.page
    }
  },
  computed: {
    formUrl: function() {
      switch(this.curPage) {
        case "SPEAKERS":
          return 'https://docs.google.com/forms/d/e/1FAIpQLSdVK0xCehD8A8FuqDuY2Keve3bad-6hk_FeWzGppIYzRvX7cg/viewform?embedded=true';
        case "VOLUNTEERS":
          return 'https://docs.google.com/forms/d/e/1FAIpQLSccKcHQF88liSADa-gCb5FczgAonG5CymO4ya9eMcH7_g6WUg/viewform?embedded=true';
        default:
          return "";
      }
    },
    formHeight: function() {
      switch(this.curPage) {
        case "SPEAKERS":
          return 1440;
        case "VOLUNTEERS":
          return 2478;
        default:
          return 0;
      }
    }
  },
  components: {
    Header,
    Form,
    AboutPage,
    DonatePage,
    Footer
  },
  methods: {
    switchPage(page) {
      this.curPage = page;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #page-content {
    margin-top: 132px;
  }
</style>
