<template lang="pug">
  header.l-container.p-globalNavi
    .l-inner.p-headerInner
      header-logo
      header-nav
</template>

<script>
import HeaderLogo from '../atoms/HeaderLogo'
import HeaderNav from '../molecules/HeaderNav'
export default {
  components: {
    HeaderLogo,
    HeaderNav
  }
}
</script>
