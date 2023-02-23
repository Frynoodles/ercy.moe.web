<script setup lang="ts">
import header_pannel from './components/Header.vue'
(function(){
  document.addEventListener('visibilitychange',function(){
    if(!document.hidden){
      // 处于当前页面
      document.title="你所热爱的就是你的生活"
    }else{
      // 不在当前页面
      document.title="(*^▽^*) ~~ 摸鱼"
    }
  })
})();
</script>

<template>
  <header_pannel />
</template>


<style scoped></style>
