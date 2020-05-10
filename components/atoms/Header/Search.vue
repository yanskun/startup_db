<template lang="pug">
  #header-search.p-search__headArea
    form.c-search__form
      input#top-search.c-search__input(
        placeholder="企業名で検索する"
        type="search"
      )
      button.c-search__btn(
        type="submit"
      )
        i.fas.fa-search.icon
</template>

<style lang="scss" scoped>
#header-search{
  display: block;
  flex-grow: 1;
}
.p-search__headArea {
  position: static;
  width: auto;
  padding: 0 0 0 32px;
  left: 3%;
}
.c-search__form {
  width: 100%;
  position: relative;
}
#top-search {
  border-radius: 4px;
  font-size: 0.75rem;
}
.c-search__input {
    width: 100%;
    padding: 7px 16px;
    background-color: #f6f7f9;
    color: #4a4a4a;
    border: 0;
    -webkit-appearance: none;
}
.c-search__btn {
  font-size: 13px;
  font-size: 0.8125rem;
  color: #3dbba3;
  position: absolute;
  top: 0;
  right: 0;
  border: 0;
  border-radius: 50%;
  background-color: transparent;
  height: 100%;
  padding: 0 16px;
}
</style>
