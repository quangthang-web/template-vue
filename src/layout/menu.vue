<template>
  <div class="navbars">
    <NavBar />
  </div>
</template>
<script>
import NavBar from "./components/Navbar.vue";
export default {
  components: {
    NavBar,
  },
};
</script>
<style lang="scss" scoped>
.navbars {
  position: fixed;
  padding: 20px 0;
  background-color: #fff;
  width: 100%;
  z-index: 999;
}
</style>
