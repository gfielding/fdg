<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style>
.home	{
	position: relative;
}
img {
	position: absolute;
	top: 10vh;
	left: 0;
	animation: move 3s 1s both ease-in-out 2;
}

@keyframes move {
	0% {
		transform: translateX(-20vw);
	}

	100% {
		transform: translateX(120vw);
	}
}
</style>
