<template>
  <v-card light>
    <div id="workMain">
      <h1 id="title" align="center">Work</h1>
      <v-container style="max-width: 800px">
        <fade-in-component>
          <section>
            <v-card>
              <v-timeline dense clipped>
                <v-timeline-item class="mb-6" hide-dot>
                  <v-row justify="space-between">
                    <v-col cols="12" sm="3" md="3"> 2002 9/16 </v-col>
                    <v-col cols="12" sm="9" md="9"> 生誕 </v-col>
                  </v-row>
                </v-timeline-item>
                <v-timeline-item
                  v-for="(item, i) in items"
                  :key="i"
                  class="mb-4"
                  :color="item.color"
                  small
                >
                  <v-row justify="space-between">
                    <v-col cols="12" sm="3" md="3">{{ item.date }}</v-col>
                    <v-col cols="12" sm="9" md="9">
                      <a :href="item.url" target="_blank" rel="noreferrer">{{
                        item.aTagContent
                      }}</a>
                      {{ item.subContent }}
                    </v-col>
                  </v-row>
                </v-timeline-item>
                <v-timeline-item hide-dot small> and now... </v-timeline-item>
              </v-timeline>
            </v-card>
          </section>
        </fade-in-component>
      </v-container>
    </div>
  </v-card>
</template>
<script>
import FadeInComponent from '../components/FadeInComponent'

export default {
  components: {
    FadeInComponent,
  },

  data: () => ({
    items: [
      {
        color: '#5BE7C4',
        date: '2018 3/4',
        url: 'https://furait.connpass.com/',
        aTagContent: 'FuraIT',
        subContent: '参加',
      },
      {
        color: '#50C1E9',
        date: '2018 4/3',
        url: 'https://www.asahikawa-nct.ac.jp/',
        aTagContent: '旭川工業高等専門学校',
        subContent: '入学',
      },
      {
        color: '#7A57D1',
        date: '2018 6/23',
        url: 'https://asahikawa.connpass.com/',
        aTagContent: '旭川ゆるい勉強会',
        subContent: '参加',
      },
      {
        color: '#5BE7C4',
        date: '2018 7/23',
        url: 'https://students.local.or.jp/',
        aTagContent: 'LOCAL学生部',
        subContent: '入部',
      },
      {
        color: '#50C1E9',
        date: '2019 1/9',
        url: 'https://twitter.com/hashtag/KosenLTONLINE?src=hashtag_click',
        aTagContent: 'Kosen LT ONLINE',
        subContent: '登壇',
      },
      {
        color: '#7A57D1',
        date: '2019 6/1',
        url: 'https://www.ospn.jp/osc2019-do/',
        aTagContent: 'OSC19do',
        subContent: '当日スタッフ',
      },
      {
        color: '#5BE7C4',
        date: '2019 8/17',
        url: 'https://conf-hokkaido.connpass.com/event/122809/',
        aTagContent: '高専カンファ in北海道',
        subContent: '司会',
      },
      {
        color: '#50C1E9',
        date: '2019 8/24',
        url: 'https://www.seccon.jp/2019/seccon_beginners/tomakomai.html',
        aTagContent: 'SECCON Beginners 2019 苫小牧',
        subContent: '参加',
      },
      {
        color: '#7A57D1',
        date: '2019 10/13',
        url: 'http://www.procon.gr.jp/?page_id=71201',
        aTagContent: '第30回高専プロコン',
        subContent: '競技部門 台風19号により辞退 参加部門敗退',
      },
      {
        color: '#5BE7C4',
        date: '2019 11/3',
        url: 'http://www.procon-asahikawa.org/',
        aTagContent: '第9回 旭川 U-16 procon',
        subContent: 'スタッフ',
      },
      {
        color: '#50C1E9',
        date: '2020 3/11',
        url: 'https://third-kosen-bcon.peatix.com/view',
        aTagContent: '第3回 高専ビジネスコンテスト by高専キャリア',
        subContent: 'チーム「よっぴー」MVT, サンケイエンジニアリング賞受賞',
      },
      {
        color: '#7A57D1',
        date: '2020 6/27',
        url: 'https://ospn.connpass.com/event/177262/',
        aTagContent: 'OSC20do',
        subContent: 'LOCAL学生部 発表',
      },
      {
        color: '#5BE7C4',
        date: '2020 11/3',
        url: 'http://www.procon-asahikawa.org/',
        aTagContent: '第10回 旭川 U-16 procon',
        subContent: 'スタッフ 実況',
      },
      {
        color: '#50C1E9',
        date: '2021 2/26',
        url: 'https://jig.jp/topics/202012252000/',
        aTagContent: '2021年冬jig.jpインターン',
        subContent: '参加',
      },
      {
        color: '#7A57D1',
        date: '2021 6/26',
        url: 'https://www.tmcseec.net/ja/cst4u25_2021',
        aTagContent: 'サイバーセキュリティTOKYO for U25',
        subContent: '参加',
      },
      {
        color: '#5BE7C4',
        date: '2021 8/16~ 27',
        url: 'https://www.lateral-t.co.jp/',
        aTagContent: 'ラテラル・シンキング株式会社 インターン',
        subContent: '参加',
      },
      {
        color: '#50C1E9',
        date: '2021 9/6~ 10',
        url:
          'https://e-seikatsu.snar.jp/jobboard/detail.aspx?id=9BjwS-eTmr6U1o1M_6Imqg',
        aTagContent: '株式会社いい生活 インターン',
        subContent: '参加',
      },
      {
        color: '#7A57D1',
        date: '2021 10/9',
        url: 'https://www.procon.gr.jp/',
        aTagContent: '第32回高専プロコン',
        subContent: '競技部門',
      },
      {
        color: '#5BE7C4',
        date: '2021 11/3',
        url: 'https://www.youtube.com/watch?v=aASXCBUuDLc&t=23807s',
        aTagContent: '第11回 旭川 U-16 procon',
        subContent: 'スタッフ 実況',
      },
    ],
  }),
}
</script>
<style scoped>
#workMain {
  padding-bottom: 50px;
}

#title {
  color: #35495e;
  padding: 20px 0px;
}

/* aタグのデコレーションを消す */
a {
  text-decoration: none;
}
</style>
