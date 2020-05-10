<template lang="pug">
  li.p-headerNavi__item
    nuxt-link(
      v-if="getPath"
      :to="option.path"
      class="is-current"
    ) {{ option.name }}
    a(
      v-else
      :href="option.path"
    ) {{ option.name }}
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
    getPath() {
      return this.option.path.charAt(0) === "/"
    }
  },
}
</script>

<style lang="scss" scoped>
.p-headerNavi__item {
  margin: 0 12px;
  a {
    font-size: 13px;
    font-size: 0.8125rem;
    padding: .8rem 0;
    font-weight: 700;
    display: block;
    color: #fff;
    word-break: keep-all;
    position: relative;
  }
}
</style>
