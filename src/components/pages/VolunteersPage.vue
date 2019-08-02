<template>
  <div id="page-content">
    <Border />
    <div class="section">
      <div class="two-third">
        <p>Welcome aboard!  We are so happy that you are willing to join with us
          as we work together to &quot;rise up&quot; from the negative stigma
          and struggles of anxiety and depression. We all have struggles, which
          often give us the gift of empathy.  This allows us to more powerfully
          help others overcome similar situations they are facing.</p>
        <p>Our youth are especially vulnerable with feelings of isolation
          and self-doubt, but with your help we can empower them and help them
          see that they are not alone! Thank you for your efforts to notice the
          one, helping them &quot;rise up&quot; to a happier, more confident
          self. We will make a difference as we reach out and reach up,
          rising up together!</p>
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
  name: 'VolunteersPage',
  data: function() {
    return {
      formUrl: 'https://docs.google.com/forms/d/e/1FAIpQLSccKcHQF88liSADa-gCb5FczgAonG5CymO4ya9eMcH7_g6WUg/viewform?embedded=true',
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
