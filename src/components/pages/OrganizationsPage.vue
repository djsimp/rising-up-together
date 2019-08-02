<template>
  <div id="page-content">
    <Border />
    <div class="section">
      <div class="two-third">
        <p>
          Welcome aboard! We are excited to work together with you to reduce
          suicide, helping our youth “rise up” from the negative stigma and
          struggles of anxiety and depression, which too often results in suicide.
        </p> 
        <p>
          One of the purposes of Rising Up Together is to bring likeminded
          organizations together that are focused on reducing suicide and/or
          to help others deal with mental illness. Rising Up Together wants
          organizations like you to join us in teaching important skills and
          habits that will empower these youth to better cope with the stresses
          of life.
        </p>
        <p>
          Please join us by filling out the form below to help us know what
          your organization does best so we can work together, giving our youth
          a safer and brighter future!
        </p>
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
  name: 'OrganizationsPage',
  data: function() {
    return {
      formUrl: 'https://docs.google.com/forms/d/e/1FAIpQLSfwB86SLG-CkbdZUz_7Y4o3X3huakTyw5lm2578M-GDCpoxCg/viewform?embedded=true',
      formHeight: 1150
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
