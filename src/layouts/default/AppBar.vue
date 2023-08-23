<template>
  <v-app-bar flat>
    <div class="icon-div">
      <v-icon class="icon" @click="emitIconClickEvent">mdi-theme-light-dark</v-icon>
    </div>
    <v-app-bar-title >
      CONNECTECH 2023: VOCÊ NO FUTURO DA TECNOLOGIA
    </v-app-bar-title>
  </v-app-bar>
</template>

<script>
export default{
  methods: {
    emitIconClickEvent() {
      this.$emit('icon-click'); 
    }
}
}
</script>

<style scoped>
.icon-div {
  display: flex;
  padding: 0 20px;
}
</style>

  
