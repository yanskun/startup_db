<template lang="pug">
  .p-advantages__item
    .p-advantages__img
      img(
        :src="option.img"
      )
    .p-advantages__text {{ option.text }}
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
.p-advantages__item {
  margin: 0 15px;
  padding: 0;
  -webkit-box-flex: 1;
  flex-grow: 1;
  min-width: 70px;
  .p-advantages__img {
    display: flex;
    -webkit-box-pack: center;
    justify-content: center;
    margin-bottom: 3px;
    img {
      width: 100%;
      height: auto;
    }
  }
  .p-advantages__text {
    color: #3dbba3;
    text-align: center;
    font-weight: 600;
    line-height: 1.6;
    transform: scale(1);
    font-size: .625rem;
    br {
      display: block;
    }
  }
}
</style>
