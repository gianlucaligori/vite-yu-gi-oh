<script>

import CardApp from './CardApp.vue';
import { store } from '../store';
export default {
  
    data() {
        return {
            store,
        }
    },

    components: {
        CardApp,
    }
}
</script>


<template lang="">
    <main>
        
        <select name="select" id="Seleziona">
            <option value="Seleziona">Seleziona</option> <!-- cambia value e testo-->
        </select>

        <div class="container">
            <CardApp/>
        </div>
    </main>
</template>


<style lang="scss" scoped>
  
  main {
    max-width: 1200px;
    border: 1px solid black;
    margin: auto;
    margin-top: 1rem;   //Poi cancella
  }
</style>