<template>
	<div class="text-writer">
		<slot></slot>
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
			// anything wrapped in line-wrapper gets animated
			var lines = this.$el.querySelectorAll(".line-wrapper");

			for (let el of lines) {
				el.innerHTML = el.textContent.replace(/\S/g, "<span class='letter'>$&</span>");
			}

			var timeline = anime.timeline();

			for (let el of lines) {
				timeline.add({
					targets: el.querySelectorAll('.letter'),
					opacity: [0, 1],
					translateY: ["1.1em", 0],
					translateZ: 0,
					duration: 750,
					delay: anime.stagger(50, { start: 500 })
				});
			}
		}
	}
</script>

<style lang="scss">
	.line-wrapper {
		position: relative;
		overflow: hidden;
	}
	
	.letter {
		display: inline-block;
		line-height: 1em;
	}
</style>