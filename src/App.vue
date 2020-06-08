<template>
<v-app>
    <NavBar></NavBar>

  <!-- Sizes your content based upon application components -->
  <v-content>
    
    
    
    <!-- Provides the application the proper gutter -->
    <v-container fluid>
      <!-- <v-row>
        <v-col cols='3'>
        <FiltruBar></FiltruBar>
        </v-col>
        <v-col cols='9'> sdasdfasdf -->

        <router-view></router-view>
        <!-- </v-col>
      </v-row> -->
    </v-container>
  </v-content>

  <v-footer app>
    <!-- -->
  </v-footer>
</v-app>
</template>
<script>
import NavBar from './components/NavBar';

export default {
  name: 'App',
  components: {
    NavBar
  },

  data: () => ({
    
   
  }),
};
</script>
