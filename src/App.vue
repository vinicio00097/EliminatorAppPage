<template>
  <v-app>
    <v-app-bar
      app
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://unknowntechnologies.github.io/EliminatorApp/assets/safety-icon.jpg"
          transition="scale-transition"
          width="40"
        />

      </div>
      <v-toolbar-title class="headline">
        <span>Eliminator</span>
      </v-toolbar-title>
      <v-spacer/>
      <v-btn icon @click="()=>{
          isDark=!isDark;
          isDark?iconDark='mdi-brightness-7':iconDark='mdi-brightness-6'
          this.$vuetify.theme.dark=isDark;
        }">
        <v-icon>{{iconDark}}</v-icon>
      </v-btn>
    </v-app-bar>
    <v-content>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    isDark:false,
    iconDark:"mdi-brightness-6"
  }),
};
</script>
<style scoped>
.inline{
    display:inline-block;
    vertical-align:middle;
}
</style>
