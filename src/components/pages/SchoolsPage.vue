<template>
  <div id="page-content">
    <Border />
    <div class="section">
      <div class="two-third">
        <p>Please join us by filling out the form below.</p>
        <Form :url="formUrl" :height="formHeight" />
      </div>
      <div class="one-third">
        <Donate />
      </div>
    </div>
  </div>
</template>

<script>
import Donate from '../Donate.vue'
import Border from '../Border.vue'
import Form from '../Form.vue'

export default {
  name: 'SchoolsPage',
  data: function() {
    return {
      formUrl: 'https://docs.google.com/forms/d/e/1FAIpQLScgBUe_cd4Y4NYaEvKwWUXWiMroxNQCZWbgxKHQTCw2Sh9uGg/viewform?embedded=true',
      formHeight: 2478
    }
  },
  components: {
    Donate,
    Border,
    Form
  }
}
</script>

<style scoped>
  .section {
    display: flex;
  }
  .two-third {
    flex-grow: 2;
    width: 67%;
  }
  .one-third {
    flex-grow: 1;
    width: 33%;
  }
  .two-third, .one-third {
    padding: 20px 40px;
  }
</style>
