<template lang="pug">
  .l-separete
    main.l-main.p-main__areaIndex
      Banner
</template>

<script>
import Banner from "../components/organisms/Banner"
export default {
  components: {
    Banner
  }
}
</script>

<style lang="scss" scoped>
.p-main__areaIndex {
  padding: 32px;
  padding-top: 0;
  padding-bottom: 0;
}
.l-main {
  min-width: 0;
  width: 100%;
  -webkit-box-ordinal-group: 3;
  order: 2;
}
</style>
