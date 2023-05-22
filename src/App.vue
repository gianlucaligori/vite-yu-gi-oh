<script>
import HeaderApp from './components/HeaderApp.vue';
import CardList from './components/CardList.vue';
import CardApp from './components/CardApp.vue';
import axios from 'axios';
import { store } from './store';

export default {
	data() {
		return {
			store,
		};
	},
	components: {
    HeaderApp,
    CardList,
    CardApp,
  	},
	created() {
		// qui fare la richiesta all'api
		axios
			.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
			.then(response => (this.store.characterList = response.data.data));
	},
};
</script>

<template>
	<div class="container">
		<h1>Yu Gi Oh</h1>

		<main>
      <HeaderApp/>
			<CardList />
			<CardApp />
		</main>
	</div>
</template>

<style lang="scss">
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

.html {
	font-family: 'Montserrat', sans-serif;
}

.container {
	margin: 0 auto;
	padding: 1rem;
	max-width: 1000px;
}

h1 {
	text-align: center;
}
</style>
