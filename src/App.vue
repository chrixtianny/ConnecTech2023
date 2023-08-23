<template>
  <div :style="{
    backgroundColor: isDarkMode ? darkBackgroundColor : lightBackgroundColor,
    color: isDarkMode ? darkTextColor : lightTextColor
  }">
  <router-view />
  </div>
</template>

<script>
  import { ref } from 'vue';

  export default {
    setup() {
      const isDarkMode = ref(false);

      const toggleDarkMode = () => {
        isDarkMode.value = !isDarkMode.value;
      };

      return {
        isDarkMode,
        toggleDarkMode
      };
    },
    data() {
      return {
        darkBackgroundColor: '#7700a6',
        darkTextColor: '#ffffff',
        lightBackgroundColor: '#fefefe',
        lightTextColor: '#29132e'
      }
    },
    mounted() {
      const prefersDarkMode = window.matchMedia('(prefers-color-scheme: dark)').matches;
      this.isDarkMode = prefersDarkMode;
    }
  }
</script>
