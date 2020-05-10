<template lang="pug">
  .p-footerSns
    ul.p-footerSns__wrap
      sns-item(
        :option="option"
        v-for="option in options"
      )
</template>

<script>
import SnsItem from "../../atoms/Footer/SnsItem"
export default {
  components: {
    SnsItem
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
          iconClass: "fa-facebook-f",
          path: "https://www.facebook.com/startupdbjp/"
        }
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.p-footerSns__wrap {
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  padding-bottom: 35px;
}
</style>
