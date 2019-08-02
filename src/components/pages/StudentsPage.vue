<template>
  <div id="page-content">
    <Border />
    <div class="section">
      <div class="two-third">
        <p>Hi there! Welcome to Rising Up Together! We are excited to work
          and do many great things with you!</p>
        <p>Rising Up Together is an organization meant for all youth!
          Here you will make great friendships, participate in fun activities
          with food, as you meet and talk together! Our goal is to provide a
          safe environment where teens, like you, can lift, build, and serve
          one another, so they can feel comfortable discussing their struggles.
          Because guess what? We have all experienced what it’s like to be in
          a R.U.T. and as we come together, we can better lift each other out
          of the R.U.T.</p>
        <p>We are excited for you to join us and see what Rising Up Together
          is all about! <strong>Sign up now!</strong></p>
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
  name: 'StudentsPage',
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
