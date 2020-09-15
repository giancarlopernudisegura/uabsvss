<template lang="pug">
div
	section.section
		h1.title About Us
		lorem(add="2p")
</template>

<script>
import LoremIpsum from 'vue-lorem-ipsum/src/LoremIpsum.vue'

export default {
	components: {
		lorem: LoremIpsum
	}
}
</script>
