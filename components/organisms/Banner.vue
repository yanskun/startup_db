<template lang="pug">
  .p-banner__area.p-banner__register
    Content
    .p-banner__img(
      :style="{ backgroundImage: 'url('+ imgUrl +')' }"
    )
</template>

<script>
import Content from "../molecules/Banner/Content"
import backgroundImg from "../../assets/images/pc_top_kv_follow_banner.jpg"
export default {
  components: {
    Content
  },
  data() {
    return {
      imgUrl: 'https://startup-db.com/images/pc_top_kv_follow_banner.jpg'
    }
  },
}
</script>

<style lang="scss" scoped>
.p-banner__register {
  margin: 0 -32px 32px;
}
.p-banner__area {
  position: relative;
  cursor: pointer;
}
.p-banner__register .p-banner__img {
  height: 240px;
  background-repeat: no-repeat;
  background-position: top;
  background-size: cover;
}
</style>
