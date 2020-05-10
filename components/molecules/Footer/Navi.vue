<template lang="pug">
  .l-inner.p-footerNavi
    ul.p-footerNavi__wrap(
      v-for="option in options"
    )
      footer-navi-item(
        :option="option"
      )
</template>

<script>
import FooterNaviItem from "../../atoms/Footer/NaviItem"
export default {
  components: {
    FooterNaviItem
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
