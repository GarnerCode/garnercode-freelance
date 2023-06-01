<template>
  <div id="home-page">
    <Landing></Landing>
    <div class="home-sections">
      <Testimonials></Testimonials>
      <Services></Services>
      <About></About>
      <Portfolio subtitle="Featured Work" featured="true"></Portfolio>
      <Contact></Contact>
    </div>
  </div>
</template>

<style lang="scss">
  @media screen and (min-width: 0px) {
    #home-page {
      .home-sections {
        display: flex;
        flex-direction: column;
        gap: 10rem;
      }
    }
  }
  @media screen and (min-width: 768px) {
    #home-page {
      .home-sections {
        display: flex;
        flex-direction: column;
        gap: 15rem;
      }
    }
  }
</style>

<script lang="ts">
import Vue from 'vue'
import Testimonials from '~/components/Testimonials.vue';

export default Vue.extend({
    name: "IndexPage",
    components: { Testimonials }
})
</script>
