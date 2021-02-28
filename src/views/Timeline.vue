<template>
  <v-timeline>
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      :color="year.color"
      small
    >
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-bold ${year.color}--text`"
          v-text="year.year"
        ></span>
      </template>
      <div class="py-4">
        <h2 :class="`headline font-weight-light mb-4 ${year.color}--text`">
          {{year.title}}
        </h2>
        <div>
          {{year.note}}
        </div>
      </div>
    </v-timeline-item>
  </v-timeline>
</template>
<script>
  export default {
    data: () => ({
      years: [
        {
          color: 'cyan',
          year: '2015/3',
          title: '大学卒業',
          note:  '文系大学を卒業、文系と言いながら少しJavaScriptを勉強していました。'
        },
        {
          color: 'green',
          year: '2015/4',
          title: '現職入社',
          note:  '入社後に研修等を行い社会人としての基礎を学ばせていただきました。'
        },
        {
          color: 'pink',
          year: '2016/6～2016/11',
          title: 'システムのVersionUpを担当',
          note:  '本案件のおかげでHTML + css + JavaScript + Java + Servletについての理解をすることができました。'
        },
        {
          color: 'amber',
          year: '2016/12～2018/3',
          title: 'awsを使用した小規模システムを開発',
          note:  '設計や開発について、一気通貫で作業することができて偏りがちななんのためにシステムを開発しているのかということに気づくことができた、とてもよい経験でした。会社内のアカウントでは自由に使用できなかったので、自分でアカウントを作成し、WordPressを用いたサービスの展開をHowTo本から学習しました。'
        },
        {
          color: 'orange',
          year: '2020/10～現在',
          title: '新システム開発中',
          note:  '今までにやってこなかったC# + Vue + TypeScript + Vuetifyを使用してサービスを立ち上げています。MVVCモデルの考え方やフロント、バックエンドの進め方など新しいことを知ることができてとても楽しいPJです。'
        },
      ],
    }),
  }
</script>