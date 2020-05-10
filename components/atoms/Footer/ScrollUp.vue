<template lang="pug">
  .p-btn__scrollUp(
    @click="onClick"
  )
    | Scroll to TOP
</template>

<script>
export default {
  methods: {
    onClick() {
      window.scrollTo({top: 0, behavior: 'smooth'});
    }
  }
}
</script>

<style lang="scss" scoped>
.p-btn__scrollUp {
  width: 100%;
  font-size: 12px;
  font-size: 0.75rem;
  -webkit-transition: .2s ease-in-out;
  -o-transition: .2s ease-in-out;
  transition: .2s ease-in-out;
  background-color: #4a4a4a;
  color: #fff;
  text-align: center;
  padding: 5px 0;
  cursor: pointer;
}
</style>
