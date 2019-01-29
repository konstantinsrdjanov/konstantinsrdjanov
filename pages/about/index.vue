<template>
	<section class="container">
		<div>
			<h1 class="title">
				About Page
			</h1>
			<h2 class="subtitle">
				About page content
			</h2>
		</div>
	</section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
	components: {
		Logo
	},

	data() {
		return {
			title: 'About | Nuxt'
		}
	},

	head() {
    	return {
      		title: this.title,
      		meta: [
        		// hid is used as unique identifier. Do not use `vmid` for it as it will not work
        		{ hid: 'ABOUT_DESCRIPTION', name: 'description', content: 'My about page description' }
      		]
    	}
  	}
}
</script>

<style>
.container {
	margin: 0 auto;
	min-height: 100vh;
	display: flex;
	justify-content: center;
	align-items: center;
	text-align: center;
}

.title {
	font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
		'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
	display: block;
	font-weight: 300;
	font-size: 100px;
	color: #35495e;
	letter-spacing: 1px;
}

.subtitle {
	font-weight: 300;
	font-size: 42px;
	color: #526488;
	word-spacing: 5px;
	padding-bottom: 15px;
}
</style>
