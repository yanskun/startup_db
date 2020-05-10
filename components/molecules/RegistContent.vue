<template lang="pug">
  .p-modal__contents
    .p-advantages(
      v-if="isRegisterd"
    )
      advantage-item(
        v-for="option in advantageOptions"
        :option="option"
      )
    register-button(
      v-for="option in snsOptions"
      :option="option"
      :isRegisterd="isRegisterd"
    )
    .u-flex__center.p-modal__text
      span または
    mail-form
    signup-form(
      :isRegisterd="isRegisterd"
    )
    registerd-text(
      :isRegisterd="isRegisterd"
      @on-click="onTextClick"
    )
</template>

<script>
import AdvantageItem from "../atoms/AdvantageItem"
import RegisterButton from "../atoms/RegisterButton"
import MailForm from "../atoms/MailForm"
import SignupForm from "../atoms/SignupForm"
import RegisterdText from "../atoms/RegisterdText"
export default {
  components: {
    AdvantageItem,
    RegisterButton,
    MailForm,
    SignupForm,
    RegisterdText
  },
  props: {
    isRegisterd: {
      type: Boolean,
      required: true
    }
  },
  data() {
    return {
      advantageOptions: [
        {
          img: "https://startup-db.com/images/advantage_point_01.svg",
          text: "企業をフォロー",
          textSec: "マイページで管理"
        },
        {
          img: "https://startup-db.com/images/advantage_point_02.svg",
          text: "フォロー企業の",
          textSec: "ニュースが届く"
        },
        {
          img: "https://startup-db.com/images/advantage_point_03.svg",
          text: "起業家/CxO登壇",
          textSec: "特別イベント招待"
        }
      ],
      snsOptions: [
        {
          buttonClass: "p-fb__btn",
          iconClass: "fa-facebook-f",
          text: "Facebook"
        },
        {
          buttonClass: "p-twitter__btn",
          iconClass: "fa-twitter",
          text: "Twitter"
        },
        {
          buttonClass: "p-google__btn",
          path: "https://startup-db.com/images/icon-google.svg",
          text: "Google"
        },
        {
          buttonClass: "p-linkedin__btn",
          iconClass: "fa-linkedin",
          text: "Linkedin"
        }
      ]
    }
  },
  methods: {
    onTextClick() {
      this.$emit('on-click')
    }
  },
}
</script>

<style lang="scss" scoped>
.p-modal__contents {
  padding: 18px 33px;
  .p-advantages {
    display: flex;
    justify-content: space-between;
    margin: 0 0 21px;
  }
  .p-modal__text {
    color: #999;
    letter-spacing: normal;
    font-size: 12px;
    font-size: .75rem;
  }
}
</style>
