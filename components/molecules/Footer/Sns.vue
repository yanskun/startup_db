<template lang="pug">
  .p-footerSns
    ui.p-footerSns__wrap(
      v-for="option in options"
    )
      footer-sns-item(
        :option="option"
      )
</template>

<script>
import FooterSnsItem from "../../atoms/Footer/SnsItem"
export default {
  components: {
    FooterSnsItem
  },
  data() {
    return {
      options: [
        {
          class: "p-twitter",
          iconClass: "fa-twitter",
          path: "https://twitter.com/startupdb_com"
        },
        {
          class: "p-facebook",
          iconClass: "fa-facebook",
          path: "https://www.facebook.com/startupdbjp/"
        }
      ]
    }
  },
}
</script>
