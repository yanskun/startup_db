  <template lang="pug">
  .p-banner__contents.u-flex__center.u-flex__col(
    @mouseenter="onMouseEnter"
    @mouseleave="onMouseLeave"
  )
    p.p-banner__text.is-title 企業をフォローして、
      br
      | 最新情報を入手しよう。
    .p-info__area
      Info(
        v-for="option in options"
        :option="option"
      )
    button.p-banner__btn.is-top(
      :class="{'hover': isHover}"
    ) 無料会員登録
</template>

<script>
import Info from "./Info"
export default {
  components: {
    Info
  },
  data() {
    return {
      isHover: false,
      options: [
        {
          class: "is-company",
          url: "https://startup-db.com/images/company_banner.svg",
          text: "企業をフォロー",
          textSec: "マイページで管理"
        },
        {
          class: "is-mail",
          url: "https://startup-db.com/images/mail_banner.svg",
          text: "フォロー企業の",
          textSec: "ニュースが届く"
        },
        {
          class: "is-group",
          url: "https://startup-db.com/images/group_banner.svg",
          text: "起業家/CxO登壇",
          textSec: "特別イベント招待"
        }
      ]
    }
  },
  methods: {
    onMouseEnter() {
      this.isHover = true
    },
    onMouseLeave() {
      this.isHover = false
    }
  },
}
</script>

<style lang="scss" scoped>
.p-banner__contents {
  padding: 25px 0 14px;
  color: #fff;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  border-bottom: 1px solid #efefef;
}
.u-flex__col {
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  flex-direction: column;
}
.u-flex__center {
  -webkit-box-pack: center;
  -webkit-justify-content: center;
  -webkit-box-align: center;
  align-items: center;
}
.p-banner__text.is-title {
  font-size: 1.25rem;
  font-weight: 700;
  line-height: normal;
  letter-spacing: normal;
  margin-bottom: 15px;
  color: #fff;
  text-align: center;
}
br {
  display: none;
}
.p-info__area {
  display: flex;
  -webkit-box-orient: horizontal;
  -webkit-box-direction: normal;
  flex-direction: row;
  box-shadow: none;
  padding: 0;
  -webkit-box-pack: start;
  justify-content: flex-start;
  -webkit-box-align: center;
  align-items: center;
  transition: all 0.3s ease-in-out;
  position: relative;
  z-index: 1;
}
.p-banner__btn {
    margin-top: 18px;
}
.p-banner__btn {
    cursor: pointer;
    border: 2px solid #fff;
    color: #fff;
    background-color: rgba(255,255,0,0);
    border-radius: 30px;
    width: 235px;
    height: 32px;
    font-size: .75rem;
    font-weight: 600;
}
.hover {
  background: #fff;
  color: #3dbba3;
}
</style>
