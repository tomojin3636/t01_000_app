<template>
  <v-app>
    <Header />
    <v-main>
      <router-view /> 
    </v-main>
    <Footer />
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import Header from '@/components/Header.vue';
import Home from '@/components/Home.vue';
import Footer from '@/components/Footer.vue';

export default Vue.extend({
  name: 'App',
  
  components: {
    Header,
    Home,
    Footer
  },

  data: () => ({
    }),
});
</script>


