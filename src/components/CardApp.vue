<script>
export default {
	props: {
		characterData: Object,
	},
};
</script>

<template>
	<div class="card">
		<img :src="characterData.card_images[0].image_url" :alt="characterData.name"/>
		<h2>{{ characterData.name }}</h2>
		<!-- <div class="species">{{ characterData.def }}</div> -->
	</div>
</template>

<style lang="scss" scoped>
.card {
	padding: 2rem 1rem;
	border: 2px solid brown;
	text-align: center;
}

img {
	// border-radius: 9em;
	max-width: 100%;
}
</style>
