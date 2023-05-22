<script>

import HeaderApp from './components/HeaderApp.vue';
import CardList from './components/CardList.vue';
import axios from 'axios';
import { store } from './store';


export default {

  data() {
    return {
      store,
    }
  },

  components: {
    HeaderApp,
    CardList,
  },

  created() {
		// qui fare la richiesta all'api
		axios
			.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
			.then(response => (this.store.cardList = response.data.data));
}
}
</script>


<template>

  <HeaderApp/>

  <CardList/>

</template>


<style lang="scss">

@use "../src/assets/styles/partials/reset" as *;
  
</style>