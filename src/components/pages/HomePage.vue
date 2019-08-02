<template>
  <div id="page-content">
    <Border />
    <div class="section">
      <div class="two-third">
        <p>Welcome to Rising Up Together where communities are coming together to
          help the youth throughout the nation! It is YOU that makes the biggest
          difference in helping these youth feel valued, accepted, and loved!
          Thank you for all you do to help these wonderful kids have a safer
          and brighter future!</p>
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

export default {
  name: 'HomePage',
  props: {
    url: String,
    height: Number
  },
  components: {
    Donate,
    Border
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
