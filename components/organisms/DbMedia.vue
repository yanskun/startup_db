<template lang="pug">
  section.p-card__header
    header.p-index__heading
      h2.p-index__title.p-icon.is-logo STARTUP DB MEDIA
    .p-media__area.p-card__body
      media-article-main(
        :option="mainOption"
      )
      .p-media__sub
        //- FIXME: おそらく sub と main で同一のコンポーネントを使うことが可能
        media-article-sub(
          v-for="option in subOptions"
          :option="option"
        )
</template>

<script>
import MediaArticleMain from "../molecules/MediaArticleMain"
import MediaArticleSub from "../molecules/MediaArticleSub"
export default {
  components: {
    MediaArticleMain,
    MediaArticleSub
  },
  data() {
    return {
      // TODO: mapAction で取得する前に、main, sub で振り分ける必要あり
      mainOption: {
        class: "main",
        title: "日本のDeepTechの火付け役リバネス丸氏と井上氏が語る「知識プラットフォームと人類の課題解決」",
        url: "https://media.startup-db.com/interview/leaveanest-maru-inoue",
        path: "https://media.startup-db.com/wp/wp-content/uploads/2020/04/image4-min-1.jpg",
        updateAt: "2020.04.23"
      },
      subOptions: [
        {
          class: "sub",
          title: "PMFの決め手は、ユーザーの利便性を考え続け、初心を忘れず、堅実にサービスを磨き込むこと",
          url: "https://media.startup-db.com/interview/rentio-miwa",
          path: "https://media.startup-db.com/wp/wp-content/uploads/2020/04/image4-min-1400x934.jpg",
          updateAt: "2020.04.07"
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.p-card__body {
  padding: 0 21px 15px;
  -webkit-box-flex: 1;
  flex-grow: 1;
}
</style>
