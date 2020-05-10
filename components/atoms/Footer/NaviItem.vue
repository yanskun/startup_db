<template lang="pug">
  li.p-footerNavi__item
    a(
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
  }
}
</script>>
