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
          Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
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
          note:  ''
        },
        {
          color: 'green',
          year: '2015/4',
          title: '現職入社',
          note:  ''
        },
        {
          color: 'pink',
          year: '2016/6～2016/11',
          title: 'パッケージのVersionUpを担当',
          note:  ''
        },
        {
          color: 'amber',
          year: '2016/12～2018/3',
          title: 'awsを使用した小規模システムを開発',
          note:  ''
        },
        {
          color: 'orange',
          year: '2020/10～現在',
          title: '新システム開発中',
          note:  ''
        },
      ],
    }),
  }
</script>