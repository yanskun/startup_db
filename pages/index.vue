<template lang="pug">
  .l-separete
    main.l-main.p-main__areaIndex
      Banner
      search-button
      daily-rank
      db-media
</template>

<script>
import Banner from "../components/organisms/Banner"
import SearchButton from "../components/atoms/SearchButton"
import DailyRank from "../components/organisms/DailyRank"
import DbMedia from "../components//organisms//DbMedia"
export default {
  components: {
    Banner,
    SearchButton,
    DailyRank,
    DbMedia
  },
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
  -webkit-box-ordinal-group: 3;
  order: 2;
}
</style>
