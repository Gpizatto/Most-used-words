<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Most used Words</v-toolbar-title>
    </v-app-bar>
    <v-content>
      <HomeComponent />
    </v-content>
  </v-app>
</template>

<script>
import HomeComponent from './components/Home'; 

export default {
  name: "appComponent",

  components: {
    HomeComponent

  },

  data: () => ({
    //
  }),
}
</script>
