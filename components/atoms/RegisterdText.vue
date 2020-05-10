<template lang="pug">
  .p-registerd__text
    span(
    ) {{ getSpanText }}
    a(
      href="#"
      @click="onClick"
    ) {{ getAText }}
</template>

<script>
export default {
  props: {
    isRegisterd: {
      type: Boolean,
      required: true
    }
  },
  computed: {
    getSpanText() {
      return this.isRegisterd ? "アカウントをお持ちですか？ " : "アカウントをお持ちでない場合 "
    },
    getAText() {
      return this.isRegisterd ? "ログイン" : "会員登録"
    }
  },
  methods: {
    onClick() {
      this.$emit('on-click')
    }
  },
}
</script>

<style lang="scss" scoped>
.p-registerd__text {
  font-size: .6875rem;
  font-weight: 600;
  color: #999;
  text-align: center;
  border-top: 1px solid #ccc;
  letter-spacing: normal;
  padding-top: 16px;
  margin-top: 18px;
}
</style>
