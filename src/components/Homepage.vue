<template>
  <div class="logo-connectech">
    <a href="https://doity.com.br/connectech2023">
    <img class="logo-connectech" src="../assets/logo.png" alt="Logo Connectech">
  </a>
  </div>
  <v-container class="container">
      <AboutEvent />
      <SponsorPlans :plans="plans_data"/>
      <ContactAndCreators />
  </v-container>
</template>

<script>
import AboutEvent from './AboutEvent.vue';
import ContactAndCreators from './ContactAndCreators.vue';
import SponsorPlans from './SponsorPlans.vue'

export default {
  components: {
    SponsorPlans,
    AboutEvent,
    ContactAndCreators
},
  data() {
    return {
      plans_data: [],
    }
  },
}
</script>

<style scoped>

.logo-connectech {
  max-width: 350px;
  margin: 0 auto;
  display: block;
}

template {
  padding: 20px;
  max-width: 1320px;
  width: 100%;
}

</style>
