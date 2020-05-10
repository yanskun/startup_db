<template lang="pug">
  .p-banner__info
    .p-info__img(
      :class="option.class"
      :style="{ backgroundImage: 'url('+ option.url +')' }"
    )
    p.p-info__text {{ option.text }}
      br
      | {{ option.textSec }}
</template>

<script>
export default {
  props: {
    option: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.p-banner__info {
  margin: 0 20px;
}
.p-banner__info .p-info__img {
  height: 70px;
  width: 70px;
  background-repeat: no-repeat;
  background-position: top;
  background-size: cover;
  margin: 0 auto 8px;
}
.p-info__text {
  font-size: .625rem;
  font-weight: 600;
  line-height: 1.5;
  text-align: center;
  letter-spacing: normal;
}
</style>
