<template lang="pug">
  li.p-footerSns__item
    a(
      :class="option.class"
      :href="option.path"
      target="_blank"
    )
      i.fab(
        :class="option.iconClass"
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
.p-footerSns__item {
  padding: 0 10px;
}
.p-footerSns__item a {
  width: 36px;
  border-radius: 50%;
  display: flex;
  padding: 9px;
  color: #9b9b9b;
  border: 1px solid #9b9b9b;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
}
</style>
