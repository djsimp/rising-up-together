<template>
  <div id="page-body">
    <Header :active-tab="curPage" @tab-switched="switchPage" />
    <HomePage v-if="curPage === 'HOME'" />
    <AboutPage v-if="curPage === 'ABOUT'" />
    <SchoolsPage v-if="curPage === 'SCHOOLS'" />
    <CounselorsPage v-if="curPage === 'COUNSELORS'" />
    <StudentsPage v-if="curPage === 'STUDENTS'" />
    <SponsorsPage v-if="curPage === 'SPONSORS'" />
    <OrganizationsPage v-if="curPage === 'ORGANIZATIONS'" />
    <SpeakersPage v-if="curPage === 'SPEAKERS'" />
    <VolunteersPage v-if="curPage === 'VOLUNTEERS'" />
    <Footer />
  </div>
</template>

<script>
import Header from "./Header.vue"
import HomePage from "./pages/HomePage.vue"
import AboutPage from "./pages/AboutPage.vue"
import SchoolsPage from "./pages/SchoolsPage.vue"
import StudentsPage from "./pages/StudentsPage.vue"
import CounselorsPage from "./pages/CounselorsPage.vue"
import SponsorsPage from "./pages/SponsorsPage.vue"
import OrganizationsPage from "./pages/OrganizationsPage.vue"
import SpeakersPage from "./pages/SpeakersPage.vue"
import VolunteersPage from "./pages/VolunteersPage.vue"
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
  components: {
    Header,
    HomePage,
    AboutPage,
    SchoolsPage,
    CounselorsPage,
    StudentsPage,
    SponsorsPage,
    OrganizationsPage,
    SpeakersPage,
    VolunteersPage,
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
</style>
