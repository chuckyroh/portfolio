<template>
	<div id="home">
		<div class="container">
			<div class="h-screen w-screen flex justify-center items-center bg-blue-100">
				<div class="header text-gray-700 font-bold">
					<p class="text-wrapper text-wrapper-01">
						<span class="text-6xl" ref="letters01">HI</span>
					</p>
					<p class="text-wrapper text-wrapper-02">
						<span class="text-6xl" ref="letters02">I'M CHARLES</span>
					</p>
					<p class="text-wrapper text-wrapper-03">
						<span class="text-6xl" ref="letters03">WELCOME</span>
					</p>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import anime from 'animejs/lib/anime.es.js';

	export default {
		data () {
			return {

			}
		},
		mounted () {
			this.$refs.letters01.innerHTML = this.$refs.letters01.textContent.replace(/\S/g, "<span class='letter'>$&</span>");
			this.$refs.letters02.innerHTML = this.$refs.letters02.textContent.replace(/\S/g, "<span class='letter'>$&</span>");
			this.$refs.letters03.innerHTML = this.$refs.letters03.textContent.replace(/\S/g, "<span class='letter'>$&</span>");

			anime.timeline()
			.add({
				targets: '.text-wrapper-01 .letter',
				translateY: ["1.1em", 0],
				translateX: ["0.55em", 0],
				translateZ: 0,
				opacity: [0, 1],
				rotateZ: [180, 0],
				duration: 1000,
				easing: "easeOutExpo",
				delay: (el, i) => 2000 + (80 * i)
			}).add({
				targets: '.text-wrapper-02 .letter',
				translateY: ["1.1em", 0],
				translateX: ["0.55em", 0],
				translateZ: 0,
				opacity: [0, 1],
				rotateZ: [180, 0],
				duration: 1000,
				easing: "easeOutExpo",
				delay: (el, i) => 80 * i
			}).add({
				targets: '.text-wrapper-03 .letter',
				translateY: ["1.1em", 0],
				translateX: ["0.55em", 0],
				translateZ: 0,
				opacity: [0, 1],
				rotateZ: [180, 0],
				duration: 1000,
				easing: "easeOutExpo",
				delay: (el, i) => 80 * i
			});
		}
	}
</script>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css?family=Josefin+Sans:400,700&display=swap');

	.header .text-wrapper {
		font-family: 'Josefin Sans', sans-serif;
		position: relative;
		// display: inline-block;
		padding-top: 0.2em;
		padding-right: 0.05em;
		padding-bottom: 0.1em;
		overflow: hidden;
	}
	.header .letter {
		transform-origin: 0 100%;
		display: inline-block;
		line-height: 1em;
	}
</style>