<template lang="pug">
section.section
	h1.title.is-spaced Contact
	h2.subtitle
		span.icon.has-text-success.fa-lg.is-medium
			fa(:icon="['fas', 'home']")
		span Address
	p(v-for='a in address') {{ a }}
	h2.subtitle
		span.icon.has-text-success.fa-lg.is-medium
			fa(:icon="['fas', 'envelope']")
		span Email
	a(:href='"mailto:" + email') {{ email }}
</template>

<style lang="sass" scoped>
.subtitle
	margin-top: 1.5rem
	margin-bottom: 0
</style>

<script>
export default {
	head: {
		title: 'Contact Us'
	},
	data() {
		return {
			address: [
				'Students\' Veteran Support Society',
				'University of Alberta',
				'11315 87th Ave',
				'Edmonton, AB T6G 2E1',
				'Canada'
			],
			email: 'svss@ualberta.ca'
		}
	}
}
</script>