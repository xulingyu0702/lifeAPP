<template>
  <footer>
    <ul class="footer" :style="{background:footerBgcolor}">
      <li  class="footer-menu" v-for="(menu,index) in menuList" :key="index">
        <router-link :to="menu.path">{{menu.title}}</router-link>
      </li>
    </ul>
  </footer>
</template>
<script>
export default {
  data() {
    return {
        // bgColor:"",
        // footerBgcolor:""
    };
  },
  props: ["menuList","footerBgcolor"],
  methods: {
      // selectMenu(menu){
      //     // console.log(menu)
      //       this.bgColor=menu.bgColor;
      //       this.$emit('changeTitle',menu)
      // }
  },
  mounted () {
    
  }
};
</script>
<style lang="scss"  scoped>
.footer {
  display: flex;
  bottom: 0;
  left: 0;
  position: fixed;
  height: 1rem;
 background-color: #e54847;
  width: 100%;
  line-height: 1rem;
  // z-index: 999;
  &-menu {
   
    flex-grow: 1;
    text-align: center;
    a {
       text-decoration: none;
      color: #ccc;
      outline: none;
      &.router-link-active {
        color: #fff;
         outline: none;
      }
    }
  }
}
</style>