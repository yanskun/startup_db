<template lang="pug">
  article.p-media__item.is-sub.js-link
    .p-header__wrap
      header.p-header
        h3.p-title
          nuxt-link(
            :to="option.url"
          ) {{ option.title }}
      .p-media__meta
        .p-rank__upDate
          span.p-rank__date {{ option.updateAt }}
    .p-media__image.p-image__4x3
      .p-image__inner(
        :style="{ backgroundImage: 'url('+ option.path +')' }"
      )
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
.p-media__item.is-sub {
  padding: 0;
  display: flex;
  .p-header__wrap {
    width: 70%;
    -webkit-box-ordinal-group: 3;
    order: 2;
    padding-left: 9px;
  }
  .p-title a {
    font-size: 0.875rem;
    padding-bottom: 3px;
    color: #4a4a4a;
    font-weight: 600;
    display: inline-block;
  }
}
.p-media__meta {
  color: #4a4a4a;
}
.p-media__image {
  width: 30%;
  -webkit-box-ordinal-group: 2;
  order: 1;
}
</style>
