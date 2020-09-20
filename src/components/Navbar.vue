<template lang="pug">
nav.navbar
	.navbar-brand
		a.navbar-item(href='/')
			.crop
				img(src='~/assets/logo.jpg')
			h3="Student's Veteran Support Society"
		a.navbar-burger(
			role='button'
			aria-label='menu'
			aria-expanded='false'
			data-target='navbarMenu'
			@click='toggle()'
			:class='{"is-active": active}'
		)
			span(v-for='_ in 3', aria-hidden='true')
	.navbar-menu#navbarMenu(:class='{"is-active": active}')
		.navbar-end
			nuxt-link.navbar-item(
				v-for='link in links'
				:key='link.text'
				:to='link.href'
			)
				span.icon.has-text-success
					fa(:icon="['fas', link.icon]")
				span {{ link.text }}
</template>

<style lang="sass">
.navbar-brand .crop
		max-width: 1.4rem
		overflow: hidden
	
		img
			max-width: initial
</style>

<script>
export default {
	name: 'Navbar',
	methods: {
		toggle() {
			this.active = !this.active
		}
	},
	data() {
		return {
			active: false,
			links: [
			{
				'href': '/',
				'text': 'About us',
				'icon': 'igloo'
			},
			{
				'href': '/events',
				'text': 'Events',
				'icon': 'calendar'
			},
			{
				'href': '/contact',
				'text': 'Contact',
				'icon': 'pen-fancy'
			}
			]
		}
	}
}
</script>
