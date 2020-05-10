<template lang="pug">
  .p-headerNavi__regist.c-btn__separate
    .p-headerNavi__login
      button.p-btn__login ログイン
    .p-headerNavi__regist
      button.p-btn__regist 会員登録
</template>

<style lang="scss" scoped>
.c-btn__separate {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-justify-content: space-around;
    -ms-flex-pack: distribute;
    justify-content: space-around;
}
.p-btn__login {
    font-weight: 600;
    font-size: 0.75rem;
    color: #fff;
    background: transparent;
    border: 0;
    margin: 0 8px;
    cursor: pointer;
}
.p-btn__regist {
    min-width: 128px;
    font-size: 13px;
    font-size: 0.8125rem;
}
.p-btn__regist {
  font-weight: 600;
  line-height: 2;
  color: #3dbba3;
  min-width: auto;
  height: 28px;
  padding: 0 12px;
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  -webkit-box-pack: center;
  -webkit-justify-content: center;
  -ms-flex-pack: center;
  justify-content: center;
  background-color: #fff;
  border: 0;
  border-radius: 19px;
  -webkit-box-shadow: 0 2px 2px 0 rgba(0,0,0,0.24), 0 0 2px 0 rgba(0,0,0,0.12);
  box-shadow: 0 2px 2px 0 rgba(0,0,0,0.24), 0 0 2px 0 rgba(0,0,0,0.12);
  cursor: pointer;
}
</style>
