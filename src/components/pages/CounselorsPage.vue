<template>
  <div id="page-content">
    <Border />
    <div class="section">
      <div class="two-third">
        <p>Welcome aboard! We are excited to work side-by-side with counselors
          like you to reduce suicide and break down the negative stigmas
          surrounding anxiety and depression.</p>
        <p>It is caring and compassionate counselors like you that make
          Rising Up Together possible. The impact you will have on these
          youth is staggering.</p> 
        <p>Our goal is to provide counselor-facilitated group sessions where
          youth can comfortably discuss their concerns with one another other,
          helping them see they are not alone, and feel supported. In this way,
          youth will be able to lift, build, and serve one another.</p>
        <p>Whether you have experience working with youth as a school counselor
          or a mental health counselor, we are excited for you to join us in
          this great endeavor!</p>
        <p>Thank you for all the time and energy you give in helping these
          youth &quot;rise up&quot; to have a safer and brighter future!</p> 
        <p>Please join us by registering or using your login to see the many
          wonderful ways you will empower these youth!</p>
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
  name: 'CounselorsPage',
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
