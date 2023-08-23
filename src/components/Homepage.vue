<template>
  <div :style="{
    backgroundColor: isDarkMode ? darkBackgroundColor : lightBackgroundColor,
    color: isDarkMode ? darkTextColor : lightTextColor
  }">
    <AppBar @icon-click="handleSwitchMode" />
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
  </div>
</template>

<script>
import AppBar from '../layouts/default/AppBar.vue';
import AboutEvent from './AboutEvent.vue';
import ContactAndCreators from './ContactAndCreators.vue';
import SponsorPlans from './SponsorPlans.vue'

export default{
  components: {
    AppBar,
    SponsorPlans,
    AboutEvent,
    ContactAndCreators
  },
  data() {
    return {
      isDarkMode: false,
      darkBackgroundColor: '#29132e',
      darkTextColor: '#ffffff',
      lightBackgroundColor: '#fefefe',
      lightTextColor: '#29132e'
    ,
      plans_data: [],
    }
  },

  mounted() {
    const prefersDarkMode = window.matchMedia('(prefers-color-scheme: dark)').matches;
    this.isDarkMode = prefersDarkMode;
  },

  methods: {
    handleSwitchMode() {
      this.isDarkMode = !this.isDarkMode;
    }
  }
}
</script>

<style scoped>

.logo-connectech {
  max-width: 350px;
  margin: 20px auto;
}

template {
  padding: 20px;
  max-width: 1320px;
  width: 100%;
}

</style>
