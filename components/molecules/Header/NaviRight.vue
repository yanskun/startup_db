<template lang="pug">
  .u-flex.p-headerNavi
    search
    regist
    secondary
    .p-close__icon(
      style="display: none;"
    )
      span.css-cancel
</template>

<script>
import Search from "../../atoms/Header/Search"
import Regist from "../../molecules/Header/Regist"
import Secondary from "../../atoms/Header/Secondary"
export default {
  components: {
    Search,
    Regist,
    Secondary
  }
}
</script>

<style lang="scss" scoped>
.p-headerNavi.u-flex {
  -webkit-box-ordinal-group: 4;
  order: 3;
}
.p-headerNavi.u-flex {
    -webkit-box-flex: 1;
    flex-grow: 1;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: end;
    justify-content: flex-end;
    flex-basis: 50%;
}
</style>
