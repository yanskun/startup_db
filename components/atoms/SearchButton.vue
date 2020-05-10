<template lang="pug">
  .p-btn__modal.is-top.is-sp
    a.c-btn データベースを検索する
</template>

<style lang="scss" scoped>
.p-btn__modal.is-top {
    margin: 14px 20px 20px;
}
.is-sp {
    display: block;
}
.p-btn__modal .c-btn {
    font-size: 0.875rem;
    font-weight: 600;
    color: #fff;
    padding: 15px;
    -webkit-box-shadow: 0 1px 2px 0 rgba(0,0,0,0.24);
    box-shadow: 0 1px 2px 0 rgba(0,0,0,0.24);
}
.c-btn {
    background-color: #3dbba3;
    border: 0;
    width: 100%;
    border-radius: 25px;
    cursor: pointer;
    position: relative;
    overflow: hidden;
    transition: .3s;
    display: block;
    text-align: center;
    -webkit-appearance: none;
}
</style>
