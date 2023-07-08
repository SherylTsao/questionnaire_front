<script>
import { RouterView } from 'vue-router'
import HeaderView from './components/Header.vue'
import FooterView from './components/Footer.vue'
import HomePage from './views/HomePage.vue'



export default {
  components: {
    HeaderView,
    FooterView,
    HomePage,


  },
  data() {
    return {
      isShow: true,
      showContent: false

    }
  },
  // beforeRouteEnter(to, from, next) {
  //   next(vm => {
  //     vm.showContent = to.path === "/home-page"; // 根据路由判断是否显示内容
  //   });
  // },
  mounted() {
    setTimeout(() => {
    this.showContent = false; // 将showContent设置为false，以隐藏HomePage组件
  }, 0);
  },
}
</script>

<template>
  <!-- <header class="flex justify-center items-center font-bold"> -->

  <div class="wrapper">
    <HeaderView />

    <div class="main-area">
      <RouterView />
    </div>
    <HomePage v-if="showContent" />

    <FooterView />

  </div>
  <!-- </header> -->
</template>

<style></style>
