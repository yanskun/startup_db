<template lang="pug">
  li.p-footerNavi__item
    a(
      :href="option.path"
      :target="isBlank"
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
    isBlank() {
      return this.option.name === "運営会社" || this.option.name === "Privacy Policy" ? "_blank" : ""
    }
  },
}
</script>

<style lang="scss" scoped>
.p-footerNavi__item {
  padding: 1px 2px;
  margin: 0 10px;
  a {
    color: #9b9b9b;
    font-size: 0.8125rem;
  }
}
</style>
