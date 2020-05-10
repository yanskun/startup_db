<template lang="pug">
  .p-media__main
    article.p-media__item.js-link.is-main
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
.p-media__main {
  width: 50%;
  -webkit-box-flex: 1;
  flex-grow: 1;
}
.is-main {
  margin-bottom: 0;
  .p-header__wrap {
    padding: 23px;
    position: absolute;
    bottom: 0;
    z-index: 1;
    background: rgba(0,0,0,0.4);
    .p-title {
      padding-bottom: 6px;
      a {
        color: #fff;
      }
    }
  }
  .p-media__meta {
    color: #fff;
  }
  .p-media__image {
    width: 100%;
  }
}
</style>
