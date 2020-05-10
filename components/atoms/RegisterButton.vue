<template lang="pug">
  .p-register_btn.u-flex__center.p-register__item(
    :class="option.buttonClass"
  )
    img(
      v-if="isNotIcon"
      :src="option.path"
      alt
    )
    i.icon.fab(
      v-else
      :class="option.iconClass"
    )
    span.text {{ getText }}
</template>

<script>
export default {
  props: {
    option: {
      type: Object,
      required: true
    },
    isRegisterd: {
      type: Boolean,
      required: true
    }
  },
  computed: {
    isNotIcon() {
      return !this.option.iconClass
    },
    getText() {
      return this.option.text + "で" + (this.isRegisterd ? "登録" : "ログイン")
    }
  },
}
</script>

<style lang="scss" scoped>
.p-register_btn {
  cursor: pointer;
  text-align: center;
  font-weight: 600;
  font-size: .875rem;
  padding: 6px 8px;
  position: relative;
  line-height: 2;
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  justify-content: space-around;
  margin-bottom: 14px;
  .text {
    width: 100%;
  }
  .icon {
    position: absolute;
    left: 35px;
      font-size: 1.25rem;
    top: 50%;
    margin-top: -10px;
  }
  img {
    position: absolute;
    width: 25px;
    left: 30px;
    top: 50%;
    margin-top: -12px;
    height: auto;
  }
}
.p-fb__btn, .p-twitter__btn {
  border-radius: 8px;
  box-shadow: 0 1px 2px 0 rgba(0,0,0,.24);
  color: #fff;
  letter-spacing: normal;
}
.p-fb__btn {
  background-color: #507cc0;
}
.p-twitter__btn {
  background-color: #64ccf1;
}
.p-google__btn {
  border-radius: 8px;
  box-shadow: 0 1px 2px 0 rgba(0,0,0,.24);
  color: #757575;
  background-color: #fff;
  letter-spacing: normal;
}
.p-linkedin__btn {
  border-radius: 8px;
  box-shadow: 0 1px 2px 0 rgba(0,0,0,.24);
  color: #fff;
  background-color: #187fb8;
  letter-spacing: normal;
}
.u-flex__center {
  -webkit-box-pack: center;
}

</style>
