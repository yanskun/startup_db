<template lang="pug">
  nav.p-headerNavi
    ul.p-headerNavi__primary
      navi-item(
        :option="option"
        v-for="option in options"
      )
</template>

<script>
import NaviItem from "../../atoms/Header/NaviItem"
export default {
  components: {
    NaviItem
  },
  data() {
    return {
      options: [
        {
          name: "DATABASE",
          path: "/"
        },
        {
          name: "MEDIA",
          path: "https://media.startup-db.com/"
        },
        {
          name: "NEWS",
          path: "/news"
        },
        {
          name: "FINANCE",
          path: "/investments"
        }
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.p-headerNavi {
  -webkit-box-ordinal-group: 3;
  order: 2;
  flex-basis: 35%;
}
.p-headerNavi {
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  width: 100%;
}
.p-headerNavi__item a::after {
  content: "";
  width: 0;
  transition: all 0.3s ease;
  border-bottom: 2px solid #fff;
  display: block;
  position: absolute;
  bottom: 0;
  left: 0;
}
.p-headerNavi__primary {
  padding-left: 3%;
  -webkit-box-pack: start;
  justify-content: flex-start;
}
.p-headerNavi__primary {
  display: flex;
  width: 100%;
}
</style>
