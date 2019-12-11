<template>
	<div id="home">
		<div class="container">
			<div class="h-screen w-screen flex justify-center items-center bg-blue-100">
				<div class="header text-gray-700 font-bold">
					<text-writer>
						<p class="line-wrapper lg:text-6xl md:text-5xl text-2xl leading-tight">HI</p>
						<p class="line-wrapper lg:text-6xl md:text-5xl text-2xl leading-tight">I'M CHARLES</p>
						<p class="line-wrapper lg:text-6xl md:text-5xl text-2xl leading-tight">A FRONT END DEVELOPER</p>
					</text-writer>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import TextWriter from '../components/TextWriter.vue';

	export default {
		components: {
			TextWriter
		},
		data () {
			return {

			}
		},
		mounted () {

		}
	}
</script>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css?family=Josefin+Sans:400,700&display=swap');

	.header {
		font-family: 'Josefin Sans', sans-serif;
	}
</style>