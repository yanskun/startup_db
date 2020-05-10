<template lang="pug">
  form
    .signup-form-group
      input.p-prof__email.p-register__email.p-register__item(
        autofocus="autofocus"
        autocomplete="email"
        type="email"
        required="required"
        placeholder="メールアドレス"
      )
</template>

<style lang="scss" scoped>
.p-register__item.p-register__email {
  margin: 16px 0;
  width: 90%;
  font-size: 1rem;
  padding: 8px 15px;
  border-radius: 4px;
  color: #4a4a4a;
  border: 1px solid #ccc;
  -webkit-appearance: none;
}
</style>
