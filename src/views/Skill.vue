<template>
  <v-card class="px-2 py-2">
  <div class="display-1 font-weight-regular text-xs-center font-italic">技術スキル</div>
  <div class="text-xs-center">
    <div v-for="(skill, index) in skill" :key="index" id="skills">
      <div class="title font-weight-light font-italic mt-3 mb-1">{{ skill.title }}</div>
        <v-chip
        outline
        color="primary"
        class="ma-2"
        v-for="(content, index) in skill.contents"
        :key="index"
        ><v-icon left>mdi-label</v-icon>
        {{ content.language }} {{ content.year}}年</v-chip>
        <v-spacer />
      </div>
    
  </div>
</v-card>
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
     skill: [
      {
        title:"フロントエンド",
        contents:[
          {
            language:'HTML',
            year:"5"
          },
          {
            language: 'HTML5',
            year: "5"
          },
          {
            language: 'css',
            year: "5"
          },
          {
            language: 'css3',
            year: "5"
          },
          {
            language: 'JavaScript',
            year: "5"
          },
          {
            language: 'Vue.js',
            year: "1"
          },
          {
            language: 'Vuetify',
            year: "1"
          }
        ]
      },
      {
        title:"バックエンド",
        contents:[
          {
            language:'Java',
            year:"5"
          },
          {
            language: 'C#',
            year: "1"
          }
        ]
      },
      {
        title:"データベース",
        contents:[
          {
            language:'SQL Server',
            year:"5"
          },
          {
            language: 'MySQL',
            year: "1"
          }
        ]
      }
    ]
    })
};


</script>
<style>

#skills{
  text-align: center;
}

</style>  