<template>
  <v-app>
    <Header />
    <v-main>
      <v-card style="height: 1500px">
        <router-view /> 
      </v-card>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import Header from '@/components/Header.vue';

export default Vue.extend({
  name: 'App',
  
  components: {
    Header
  },

  data: () => ({
    }),
});
</script>


