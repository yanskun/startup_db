<template lang="pug">
  article.p-rank__item.swiper-slide.swiper-slide-active(
    style="width: 214px;"
  )
    nuxt-link(
      :to="option.url"
    )
      .p-logo__wrap
        .p-logo(
          :style="{ backgroundImage: 'url('+ noImg +')' }"
        )
    h3.p-name
      nuxt-link(
        :to="option.url"
      ) {{ option.name }}
    ranking-cont(
      :option="option"
    )
</template>

<script>
import RankingCont from "./RankingCont"
export default {
  components: {
    RankingCont
  },
  props: {
    option: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      noImg: "https://startup-db.com/images/news-noimage.png"
    }
  },
}
</script>

<style lang="scss" scoped>
.p-rank__item {
  .p-logo__wrap {
    position: relative;
    width: 100%;
    height: auto;
    background: #fff;
    border: 1px solid #ccc;
    border-radius: 4px;
    &:before {
      content: "";
      display: block;
      padding-top: 100%;
    }
  }
  .p-name {
    font-size: 0.75rem;
    font-weight: 600;
    padding: 15px 0;
    height: 60px;
    display: flex;
    -webkit-box-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    align-items: center;
    a {
      display: -webkit-box;
      -webkit-box-orient: vertical;
      -webkit-line-clamp: 2;
      overflow: hidden;
      color: #4a4a4a;
    }
  }
}
.p-logo {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 4px;
  background-color: #fff;
  background-position: center;
  background-repeat: no-repeat;
  background-size: 70%;
}
.swiper-slide {
  flex-shrink: 0;
  height: 100%;
  position: relative;
}
.p-rank__item {
  padding: 0 9px;
  min-width: 120px !important;
}
</style>
