<template lang="pug">
  header.l-container.p-globalNavi
    .l-inner.p-headerInner
      logo
      navi-left
</template>

<script>
import Logo from '../atoms/Header/Logo'
import NaviLeft from '../molecules/Header/NaviLeft'
export default {
  components: {
    Logo,
    NaviLeft
  }
}
</script>
