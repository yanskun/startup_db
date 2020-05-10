<template lang="pug">
  .p-icon__close(
    @click="onClick"
  )
    i.fas.fa-times
</template>

<script>
export default {
  methods: {
    onClick() {
      this.$emit("on-click")
    }
  }
}
</script>

<style lang="scss" scoped>
.p-icon__close {
  position: absolute;
  right: 5%;
  line-height: 1;
  cursor: pointer;
}
</style>
