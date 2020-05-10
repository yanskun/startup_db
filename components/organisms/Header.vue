<template lang="pug">
  header.l-container.p-globalNavi
    .l-inner.p-headerInner
      logo
      navi-left
      navi-right
</template>

<script>
import Logo from '../atoms/Header/Logo'
import NaviLeft from '../molecules/Header/NaviLeft'
import NaviRight from '../molecules/Header/NaviRight'
export default {
  components: {
    Logo,
    NaviLeft,
    NaviRight
  }
}
</script>

<style lang="scss" scoped>
.p-globalNavi {
  box-shadow: 0 4px 4px 0 rgba(0,0,0,0.24), 0 0 4px 0 rgba(0,0,0,0.12);
  background: linear-gradient(45deg, #41B9BD 0%, #3ABE89 100%) fixed;
  position: relative;
  z-index: 100;
}
.l-container {
  width: 100%;
}
.p-headerInner {
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  -webkit-box-pack: justify;
  justify-content: space-between;
  width: 100%;
}
</style>
