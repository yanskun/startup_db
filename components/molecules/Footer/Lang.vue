<template lang="pug">
  .p-footerLang
    label.p-select__label.is-arrow__lg
      select.p-select__area
        option(
          v-for="option in options"
          :value="option.value"
        ) {{ option.label }}
</template>

<script>
export default {
  data() {
    return {
      options: [
        {
          label: "日本語",
          value: "/"
        },
        {
          label: "English",
          value: "/en/"
        }
      ]
    }
  },
}
</script>
