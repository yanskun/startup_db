<template lang="pug">
  nav.p-headerNavi
    ul.p-headerNavi__primary(
      v-for="option in options"
    )
      nav-link(
        :option="option"
      )
</template>

<script>
import NavLink from "../atoms/NavLink"
export default {
  components: {
    NavLink
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
.p-headerNavi__primary .p-headerNavi__item a::after {
  content: "";
  width: 0;
  -webkit-transition: all 0.3s ease;
  -o-transition: all 0.3s ease;
  transition: all 0.3s ease;
  border-bottom: 2px solid #fff;
  display: block;
  position: absolute;
  bottom: 0;
  left: 0;
}
</style>
