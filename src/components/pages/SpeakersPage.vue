<template>
  <div id="page-content">
    <Border />
    <div class="section">
      <div class="two-third">
        <p>Welcome aboard! We are so happy that you are willing to join with us
          to help reduce youth suicide by helping our nation’s youth
          &quot;rise up&quot; from the negative stigmas and struggles of anxiety
          and depression. We need speakers like you who are authentic, engaging,
          and have the knowledge and experience of struggling with suicidal
          thoughts and/or mental illness. We need speakers that can share their
          inspiring stories of how they overcame or are still overcoming the
          R.U.T.s of life. Thank you for caring about these wonderful youth
          and making a positive difference by joining Rising Up Together!
          We know that with your help, these youth will have a safer and
          brighter future ahead of them!</p>
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
  name: 'SpeakersPage',
  data: function() {
    return {
      formUrl: 'https://docs.google.com/forms/d/e/1FAIpQLSdVK0xCehD8A8FuqDuY2Keve3bad-6hk_FeWzGppIYzRvX7cg/viewform?embedded=true',
      formHeight: 1450
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
