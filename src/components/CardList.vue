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
    <div class="bg-container">

    <select name="" id="">
        <option value="">Seleziona qui</option>
    </select>


    <div class="cards-container">
        <CardApp
            v-for="(card, index) in store.cardList"
            :key="index"
            class="card-character"
            :card="card"
        />
    </div>

</div>

</template>

<style lang="scss" scoped>


select {
    margin: 2rem;
}
.bg-container {
    background-color: rgb(212,143,56);
}

.cards-container {
	display: flex;
	flex-wrap: wrap;
    margin-top: 2rem;
    background-color: bisque;
    max-width: 80%;
    margin: auto;
}

.card-character {
	flex: 0 0 25%;
}
</style>
