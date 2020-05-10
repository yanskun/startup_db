<template lang="pug">
  .l-separete
    aside#modal.l-aside.p-aside__area.js-modal
    RegistModal(
      :modalShow="registModalShow"
      @close-modal="closeRegistModal"
    )
    main.l-main.p-main__areaIndex
      Banner(
        @on-click="openRegistModal"
      )
      search-button
      daily-rank
      db-media
</template>

<script>
import Banner from "../components/organisms/Banner"
import SearchButton from "../components/atoms/SearchButton"
import DailyRank from "../components/organisms/DailyRank"
import DbMedia from "../components//organisms//DbMedia"
import RegistModal from '../components/organisms/Modal/Regist'
export default {
  components: {
    Banner,
    SearchButton,
    DailyRank,
    DbMedia,
    RegistModal
  },
  data() {
    return {
      registModalShow: false
    }
  },
  methods: {
    openRegistModal() {
      this.registModalShow = true
    },
    closeRegistModal() {
      this.registModalShow = false
    }
  },
}
</script>

<style lang="scss" scoped>
.p-aside__area {
  background-color: #fff0;
  box-shadow: 0 16px 16px 0 rgba(0,0,0,0.24), 0 0 16px 0 rgba(0,0,0,0.18);
  position: relative;
  z-index: 2;
}
.l-aside {
  max-width: 290px;
  -webkit-box-ordinal-group: 2;
  order: 1;
  width: 100%;
}
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
