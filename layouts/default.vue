<template>
  <v-app>
    <navbar/>
    <v-content>
      <nuxt />
    </v-content>
    <Footer/>
  </v-app>
</template>

<script>
import navbar from '~/components/globals/navbar.vue'
import Footer from '~/components/globals/footer.vue'

export default {
  components: {
    navbar,
    Footer
  }
}
</script>

<style>
/* elements */

/* fonts */


/* Spacing */


/* fonts and colors */

/* responsive */
@media (max-width: 600px) {
  .display-3 {
    font-size: 38px !important;
  }
  .display-2 {
    font-size: 34px !important;
  }
  .display-1 {
    font-size: 24px !important;
  }
  .mt-5 {
    margin-top: 24px !important;
  }
  .mb-5 {
    margin-bottom: 24px !important;
  }
  .ml-5 {
    margin-left: 24px !important;
  }
  .mr-5 {
    margin-right: 24px !important;
  }
}

</style>
