<template lang="pug">
div
	section.section
		h1.title About Us
		lorem(add="2p")
	section.section
		h1.title Instagram
</template>

<script>
import LoremIpsum from 'vue-lorem-ipsum/src/LoremIpsum.vue'

export default {
	head: {
		title: 'About Us'
	},
	components: {
		lorem: LoremIpsum
	}
}
</script>
