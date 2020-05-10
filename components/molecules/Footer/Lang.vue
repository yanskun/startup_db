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

<style lang="scss" scoped>
.p-footerLang {
  margin: 0;
}
.p-select__label {
  font-size: 0.625rem;
  color: #9b9b9b;
  position: relative;
}
.p-footerLang .p-select__area {
  border: 1px solid #979797;
  padding: 6px 30px 6px 30px;
  font-size: 12px;
  font-size: 0.75rem;
  color: #4a4a4a;
  border-radius: 4px;
}
</style>
