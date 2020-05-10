<template lang="pug">
  .l-inner.p-footerNavi
    ul.p-footerNavi__wrap
      navi-item(
        v-for="option in options"
        :option="option"
      )
</template>

<script>
import NaviItem from "../../atoms/Footer/NaviItem"
export default {
  components: {
    NaviItem
  },
  data() {
    return {
      options: [
        {
          name: "STARTUP DBについて",
          path: "https://media.startup-db.com/about"
        },
        {
          name: "お知らせ",
          path: "https://media.startup-db.com/press"
        },
        {
          name: "コミュニティ",
          path: "https://media.startup-db.com/community"
        },
        {
          name: "運営会社",
          path: "https://forstartups.com/"
        },
        {
          name: "Privacy Policy",
          path: "https://forstartups.com/privacy-policy/"
        },
        {
          name: "利用規約",
          path: "https://media.startup-db.com/terms/"
        },
        {
          name: "お問い合わせ",
          path: "https://media.startup-db.com/contact"
        }
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.p-footerNavi__wrap {
    display: flex;
    -webkit-box-pack: center;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    flex-direction: row;
    justify-content: center;
    padding-bottom: 30px;
}
</style>
