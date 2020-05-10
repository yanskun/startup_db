<template lang="pug">
  section.p-card__header
    header.p-index__heading
      h2.p-index__title.p-icon.is-dailyrank デイリーアクセスランキング
    #slider.swiper-container.swiper-container-initialized.swiper-container-horizontal
      .p-rank__area.swiper-wrapper
        ranking-article(
          v-for="option in options"
          :option="option"
        )
</template>

<script>
import RankingArticle from "../molecules/RankingArticle"
export default {
  components: {
    RankingArticle
  },
  data() {
    return {
      options: [
        {
          name: "ジェネシスヘルスケア",
          url: "/ja/companies/4929/genesis-healthcare",
          category: "pressrelease",
          updatedAt: "2019.07.12",
          desc: "遺伝子検査のパイオニア、ジェネシスヘルスケアがサッカーファン応援キャンペーン",
          site: "https://prtimes.jp/main/html/rd/p/000000062.000008653.html",
          origin: "掲載元：PR TIMES",
        },
        {
          name: "ToposWare",
          url: "/ja/companies/18965/toposwar",
          category: "news",
          updatedAt: "2020.05.08",
          desc: "DHU、学発ベンチャー「ToposWare」シードラウンドで約2億円の資金調達",
          site: "https://ict-enews.net/2020/05/08toposware/",
          origin: "掲載元：ICT教育ニュース"
        }
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.swiper-container {
  margin: 0 auto;
  position: relative;
  overflow: hidden;
  list-style: none;
  padding: 0;
  z-index: 1;
  .swiper-wrapper {
    position: relative;
    width: 100%;
    height: 100%;
    z-index: 1;
    display: flex;
    transition-property: transform, -webkit-transform;
    box-sizing: content-box;
  }
}
</style>
