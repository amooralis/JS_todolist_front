<template>
  <div id="app">
    <div class="page-content"></div>
    <component :is="layout">
      <router-view/>
    </component>
  </div>
</template>

<script>
import MainLayout from "@/layouts/MainLayout";
import AuthLayout from "@/layouts/AuthLayout";

export default {
  name: "App",
  components: {
    MainLayout,
    AuthLayout,
  },
  computed:{
    layout(){
      return this.$route.meta?.layout
    }
  }
};
</script>


<style scoped>
#app{
  background-color: wheat;
  width: 100%;
  height: 800px;
}
</style>