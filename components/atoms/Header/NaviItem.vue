<template lang="pug">
  li.is-current
    nuxt-link(
      v-if="getPath"
      :to="option.path"
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
