<template lang="pug">
  .p-modal__regist(
    v-if="isShow"
  )
    .p-modalRay
    .p-modal__area.is-regist__default
      .p-modal__header.p-modal__icon(
        :style="{ backgroundImage: 'url('+ bgImg +')' }"
      )
        h2.p-modal__title {{ getTitle }}
        close-button
      regist-content(
        @on-click="onClick"
        :isRegisterd="isRegisterd"
      )
</template>

<script>
import CloseButton from "../../atoms/CloseButton"
import RegistContent from "../../molecules/RegistContent"
export default {
  components: {
    CloseButton,
    RegistContent
  },
  data() {
    return {
      isShow: true,
      isRegisterd: true,
      bgImg: "https://startup-db.com/images/bg_startupdb.png",
    }
  },
  computed: {
    getTitle() {
      return this.isRegisterd ? "会員登録" : "ログイン"
    }
  },
  methods: {
    onClick() {
      this.isRegisterd = !this.isRegisterd
    }
  }
}
</script>

<style lang="scss" scoped>
.p-modal__regist {
  position: fixed;
  z-index: 100;
  top: 0;
  width: 100vw;
  height: 100%;
  overflow-y: scroll;
  .p-modalRay {
    position: fixed;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,.2);
    z-index: 1;
  }
  .p-modal__area {
    position: absolute;
    margin: 4% auto;
    z-index: 3;
    width: 400px;
    background: #fff;
    left: 0;
    right: 0;
    box-shadow: 0 16px 16px 0 rgba(0,0,0,.24), 0 0 16px 0 rgba(0,0,0,.18);
    border-radius: 8px;
    letter-spacing: normal;
    .p-modal__header {
      background-image: url(/images/bg_startupdb.png);
      background-size: cover;
      color: #fff;
      font-weight: 600;
      text-align: center;
      padding: 19px 0;
      border-radius: 8px 8px 0 0;
      font-size: 20px;
      font-size: 1.25rem;
    }
    .p-modal__title {
      -webkit-box-flex: 1;
      flex-grow: 1;
    }
    .p-modal__icon {
      position: relative;
      display: flex;
      -webkit-box-align: center;
      align-items: center;
    }
  }
}
</style>
