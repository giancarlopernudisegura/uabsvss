<template lang="pug">
div
	Navbar
	Nuxt
</template>

<style lang="sass">
section.section
	margin: auto
	max-width: 800px
</style>

<script>
import Navbar from '~/components/Navbar.vue'

export default {
	components: {
		Navbar
	}
}
</script>
