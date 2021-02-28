<template>
  

      <v-row dense>
            
        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
        >
          <v-card
            :color="item.color"
            dark
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="headline"
                  v-text="item.title"
                ></v-card-title>
                <v-card-subtitle v-if="item.subtile !=''"
                  v-text="item.subtitle"
                ></v-card-subtitle>
                <v-card-actions>
                   <v-btn text :href="item.link" target="_blank">
                    <v-icon v-if="item.icon != ''">{{item.icon}}</v-icon>
                    <span v-text="item.title"></span> 
                  </v-btn>
                </v-card-actions>
              </div>
            </div>
          </v-card>
        </v-col>
      </v-row>
    
   
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
/*
@Component({
  components: {
    
  },
})*/
export default  {

data: () => ({
      items: [
        {
          color: '#1F7087',
          title: 'GitHub',
          subtitle: '',
          icon: 'mdi-github',
          link: 'https://github.com/tomojin3636'
        },
        {
          color: '#55c500',
          title: 'Qiita',
          subtitle: '',
          icon: '',
          link: 'https://qiita.com/tomojin3636'
        },
        {
          color: '#1DA1F2',
          title: 'Twiiter',
          subtitle: 'お問い合わせはこちらのDMで承ります',
          icon: 'mdi-twitter',
          link: 'https://twitter.com/akira29822341'
        },
      ],
    }),
}

</script>
<style>


</style>  