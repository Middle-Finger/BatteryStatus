<template>
   
    <div class="home">
    <div><circle-loading /></div>
    <div><bubble-loading /></div>
    <div><teacup-loading /></div>
    <div><floating-button /></div>
    <view><battery-loading /></view>
</div>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import CircleLoading from './components/CircleLoading.vue'
import BubbleLoading from './components/BubbleLoading.vue'
import TeacupLoading from './components/TeacupLoading.vue'
import FloatingButton from './components/FloatingButton.vue'
import BatteryLoading from './components/BatteryLoading.vue'



export default {
  name: 'App',
  components: {
    CircleLoading,
    BubbleLoading,
    TeacupLoading,
    FloatingButton,
    BatteryLoading

  },
  onLoad() {
			console.log('app加载')
		},
		onShow() {
			console.log('app展示')
		},
		onHide() {
			console.log('app隐藏了一下')
		}
		
}
</script>

<style>
html,
body
#app {
  position: relative;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100%;
    width: 100%;
		background-color: #000;

}
</style>
