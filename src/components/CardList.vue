<script>
import CardApp from './CardApp.vue';
import { store } from '../store';

export default {
	data() {
		return {
			store,
		};
	},
	components: {
		CardApp,
	},
};
</script>

<template>
	<div class="cards-container">
		<CharacterCard
			v-for="character in store.characterList"
			:key="character.id"
			class="card-character"
			:characterData="character"
		/>
	</div>
</template>

<style lang="scss" scoped>
.cards-container {
	display: flex;
	flex-wrap: wrap;
}

.card-character {
	flex: 0 0 25%;
}
</style>
