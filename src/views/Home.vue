<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <div class="bg-video">
      <video class="bg-video__content" autoplay muted loop repeat>
        <source src="https://firebasestorage.googleapis.com/v0/b/fdg-base.appspot.com/o/coverr-ocean-and-footsteps-1559889043636.mp4?alt=media&token=bea61460-9cb2-4377-afd1-599ef6c381a3" type="video/mp4">
 
      </video>
    </div>
    <div class="circle"></div>
  </div>
</template>

<script>

export default {
  name: 'Home',
}
</script>

<style>
* {
	padding: 0;
	margin:0;
}
.home	{
	position: relative;
	height: 100vh;
	
}
.bg-video {
	position: absolute;
	height: 100vh;
	width: 100%;
	top: 0;
	left: 0;
	z-index: 0;
}
.bg-video__content {
	height: 100vh;
	width: 100%;
	object-fit: cover;
}
img {
	position: absolute;
	top: 10vh;
	left: 0;
	z-index: 1;
	animation: move 3s 1s both ease-in-out 2;
}
.circle {
	position: absolute;
	bottom:10vh;
	right:5vw;
	background-color: rgba(255,255,255,0.6);
	width: 30vw;
	height: 30vw;
	border-radius: 50%;
	z-index: 2;
	animation: circle-in 2s 1s both;
}

@keyframes move {
	0% {
		transform: translateX(-20vw);
	}

	100% {
		transform: translateX(120vw);
	}
}

@keyframes circle-in {
	0% {
		transform: translateX(25vw);
								width: 10vw;
								height: 10vw;
								opacity: 0;
	}

	100% {
		transform: translateX(0vw);
		width: 30vw;
		opacity:1;
	}
}
</style>
