<script setup lang="ts">
import Header from './components/Header.vue';
import Body__ from './components/Body.vue';
import Footer from './components/Footer.vue';

(function () {
  document.addEventListener('visibilitychange', function () {
    if (!document.hidden) {
      // 处于当前页面
      document.title = "你所热爱的就是你的生活"
    } else {
      // 不在当前页面
      document.title = "(*^▽^*) ~~ 摸鱼"
    }
  })
})();
</script>

<template>
  <Header />
  <Body__ />
  <Footer />
</template>


<style scoped></style>
