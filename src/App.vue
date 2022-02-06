<template>
  <div>
    <Menu />
    <router-view />
  </div>
</template>
<script>
import Menu from "./layout/menu.vue";
export default {
  components: {
    Menu,
  },
};
</script>
<style></style>
