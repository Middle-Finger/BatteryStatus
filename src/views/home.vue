<template>
  <div class="home">
    <div><circle-loading /></div>
    <div><bubble-loading /></div>
  </div>
</template>

<script>
import CircleLoading from '@/components/CircleLoading.vue';
import BubbleLoading from '@/components/BubbleLoading.vue';
export default {
    components: {
        CircleLoading,
        BubbleLoading
    }
}
</script>

<style>
  .home {
    display: grid;
    grid-template-columns: repeat(2,1fr);
    grid-template-rows: repeat(3, 1fr);
    height: 100vh;
    justify-items: center;
    align-items: center;
    max-width: 800px;
    margin:0 auto;
  }
  .home > div {
    transform: scale(1.5);
  }
</style>