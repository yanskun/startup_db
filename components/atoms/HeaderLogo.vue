<template lang="pug">
  header.p-headerLogo
    nuxt-link(
      to="/"
    )
      h1.p-siteTitle
        | STARTUP DB
</template>

<script>
import LogoImg from '../../assets/images/logo-white.svg'
export default {
  data() {
    return {
      img: LogoImg
    }
  }
}
</script>
