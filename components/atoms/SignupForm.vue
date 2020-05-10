<template lang="pug">
  .signup-form-group
    button.c-btn.p-register_btn.p-register__item(
      type="submit"
    ) {{ getText }}
</template>

<script>
export default {
  props: {
    isRegisterd: {
      type: Boolean,
      required: true
    }
  },
  computed: {
    getText() {
      return this.isRegisterd ? "登録する" : "ログインする"
    }
  }
}
</script>

<style lang="scss" scoped>
.p-register_btn.c-btn {
  border-radius: 30px;
  box-shadow: 0 1px 2px 0 rgba(0,0,0,.24);
}
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
}
.c-btn {
  background-color: #3dbba3;
  color: #fff;
  border: 0;
  width: 100%;
  overflow: hidden;
  transition: .3s;
  -webkit-appearance: none;
}
</style>
