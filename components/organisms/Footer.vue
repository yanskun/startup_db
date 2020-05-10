<template lang="pug">
  footer.p-footer__area
    scroll-up
    .p-footer__wrap
      navi
      sns
      lang
    copy-right
</template>

<script>
import ScrollUp from '../atoms/Footer/ScrollUp'
import Navi from '../molecules/Footer/Navi'
import Sns from '../molecules/Footer/Sns'
import Lang from '../molecules/Footer/Lang'
import CopyRight from '../molecules/Footer/CopyRight'
export default {
  components: {
    ScrollUp,
    Navi,
    Sns,
    Lang,
    CopyRight
  }
}
</script>

<style lang="scss" scoped>
.p-footer__area {
    background-color: #333;
}
.p-footer__wrap {
  padding: 30px 0 10px;
  text-align: center;
}
</style>
