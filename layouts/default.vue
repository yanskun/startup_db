<template lang="pug">
  div
    Header
    RegistModal
    nuxt
    Footer
</template>

<script>
import Header from '../components/organisms/Header'
import Footer from '../components/organisms/Footer'
import RegistModal from '../components/organisms/Modal/Regist'
export default {
  components: {
    Header,
    Footer,
    RegistModal
  }
}
</script>
