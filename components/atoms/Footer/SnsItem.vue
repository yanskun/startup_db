<template lang="pug">
  li.p-footerSns__item
    a(
      :class="option.class"
      :href="option.path"
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
  display: block;
  width: 36px;
  border-radius: 50%;
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  padding: 9px;
  color: #9b9b9b;
  border: 1px solid #9b9b9b;
  -webkit-box-pack: center;
  -webkit-justify-content: center;
  -ms-flex-pack: center;
  justify-content: center;
}
</style>
