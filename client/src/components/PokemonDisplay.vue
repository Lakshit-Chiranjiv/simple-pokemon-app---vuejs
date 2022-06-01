<template>
<!-- eslint-disable -->
  <div class="pokemon-display">
      <PokemonCard v-for="a in pokemonList" :name="a.name" :type="a.type" :power="a.power" :openUpdateModal="openUpdateModal" :openDeleteModal="openDeleteModal" :hidePokemonList="hidePokemonList" :setUpdatePokemonName="setUpdatePokemonName" :setUpdatePokemonType="setUpdatePokemonType" :setUpdatePokemonPower="setUpdatePokemonPower" :setDeletePokemonName="setDeletePokemonName" :closeOpsPanel="closeOpsPanel"/>
  </div>
  <button @click="chkclick">filter check</button>
</template>

<script>
import testData from '../testData'
import PokemonCard from './PokemonCard.vue'

export default {
    props: ['openUpdateModal','openDeleteModal','hidePokemonList','setUpdatePokemonName','setUpdatePokemonType','setUpdatePokemonPower','setDeletePokemonName','closeOpsPanel','activeSearchField','searchText'],
    data() {
        return {
            pokemonList: testData,
            filterList: (this.activeSearchField === 'name')?
                        testData.filter(p => p.name.toLowerCase().includes(this.searchText.toLowerCase())):
                        testData.filter(p => p.type.toLowerCase().includes(this.searchText.toLowerCase()))
        };
    },
    methods: {
        chkclick(){
            // console.log(this.filterList);
            console.log(this.searchText)
        }
    },
    components: { PokemonCard }
}
</script>

<style scoped>
.pokemon-display{
    display: flex;
    flex-wrap: wrap;
}
</style>