<template>
    <v-card>
        <v-navigation-drawer app v-model="drawer" clipped>
          <v-container>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title class="title">
                  Menu
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-divider></v-divider>
              <v-list nav dense>
                <v-list-item-group
                  v-model="group"
                  active-class="deep-purple--text text--accent-4"
                >
                  <v-list-item v-for="(menuItem, index) in menuItems" :key="index" :to="menuItem.url">
                    <v-list-item-icon>
                      <v-icon>{{ menuItem.icon }}</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>{{ menuItem.name }}</v-list-item-title>
                  </v-list-item>
                </v-list-item-group>
              </v-list>
          </v-container>
            </v-navigation-drawer>
        <v-app-bar
          app
          clipped-left
          color="primary"
          dark
          shrink-on-scroll
          prominent
          src="https://picsum.photos/1920/1080?random"
          fade-img-on-scroll
        >
          <template v-slot:img="{ props }">
            <v-img
              v-bind="props"
              gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)"
            ></v-img>
          </template>

          <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
          <v-app-bar-title>Tomojin</v-app-bar-title>
          <v-tabs >
              <v-tab
                v-for="(menuItem, index) in menuItems"
                :key="index"
                :to="menuItem.url"
              >
                {{ menuItem.name }}
              </v-tab>
            </v-tabs>

          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon>mdi-heart</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        
        </v-app-bar>
      
    </v-card>
</template>

<script lang="ts">
import constants from '@/common/constants'

export default {
 
 
 
  data: () => ({
      drawer: false,
      group: null,
      menuItems: constants.menuItems
    }),
};
</script>
<style>

    .v-app-bar-title__content {
        overflow: visible !important;
        margin-right: 50px !important;
    }
    
</style>
<style lang="scss" scoped>

    @import "@/styles/common/global.scss";
    .v-app-bar-title__content {
        overflow: visible !important;
        margin-right: 50px !important;
    }
    .v-app-bar__nav-icon {
      @include display_pc {
          display: none !important;
      }
    }

    .v-tabs {
      display: none;

      @include display_pc {
          display: block !important;
      }
    }

</style>