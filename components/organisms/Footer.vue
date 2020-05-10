<template lang="pug">
  footer.p-footer__area
    .p-btn__scrollUp
    footer-navi
    .p-footer__wrap
      footer-sns
      footer-lang
    copy-right
</template>

<script>
import FooterNavi from '../molecules/Footer/Navi'
import FooterSns from '../molecules/Footer/Sns'
import FooterLang from '../molecules/Footer/Lang'
import CopyRight from '../molecules/Footer/CopyRight'
export default {
  components: {
    FooterNavi,
    FooterSns,
    FooterLang,
    CopyRight
  }
}
</script>

<style lang="scss" scoped>
.p-footer__wrap {
  padding: 30px 0 10px;
  text-align: center;
}
</style>
