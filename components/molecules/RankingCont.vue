<template lang="pug">
  .p-rank__conts
    h4.p-title__category 最新ニュース
    .p-rank__meta
      .p-rank__date {{ option.updatedAt }}
      .p-rank__category(
        :class="getCategoryClass"
      ) {{ getCategoryTitle }}
    p.p-rank__desc
      a(
        target="_blank"
      ) {{ option.desc }}
    .p-rank__quotation
      a(
        target="_blank"
        :href="option.site"
      ) {{ option.origin }}
</template>

<script>
export default {
  props: {
    option: {
      type: Object,
      required: true
    }
  },
  computed: {
    getCategoryClass() {
      return "is-" + this.option.category
    },
    getCategoryTitle() {
      if (this.option.category === "pressrelease") {
        return "プレスリリース"
      } else if (this.option.category === "news") {
        return "ニュース"
      }
    }
  },
}
</script>

<style lang="scss" scoped>
.p-title__category {
  font-size: 11px;
  font-size: 0.6875rem;
  font-weight: 600;
  text-align: left;
  padding: 3px 0;
  border-bottom: 1px solid #9b9b9b;
}
.p-rank__meta {
    display: flex;
    -webkit-box-pack: justify;
    justify-content: space-between;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    flex-direction: row;
    padding: 6px 0;
  .p-rank__date {
    font-size: 0.6875rem;
  }
  .p-rank__category {
    font-size: 0.625rem;
    padding: 0 4px;
    color: #fff;
    &.is-pressrelease {
      background-color: #ff8800;
    }
    &.is-news {
      background-color: #4a90e2;
    }
  }
}
.p-rank__desc {
  font-size: 0.6875rem;
  line-height: 2;
  a {
    color: #4a4a4a;
    display: block;
  }
}
.p-rank__quotation a {
  font-size: 0.6875rem;
}
</style>
