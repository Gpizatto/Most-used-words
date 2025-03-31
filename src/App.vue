<template>
  <v-app>
    <v-main>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Most used Words</v-toolbar-title>
      
    </v-app-bar>
    
   
      <HomeComponent />
    </v-main>
  </v-app>
</template>

<script>
import HomeComponent from './components/Home'; 

export default {
  name: "appComponent",

  components: {HomeComponent},

}
</script>
