<template>
<!-- eslint-disable -->
  <div class="pokemon-display">
      <PokemonCard v-for="a in pokemonList" :name="a.name" :type="a.type" :power="a.power" :openUpdateModal="openUpdateModal" :openDeleteModal="openDeleteModal" :hidePokemonList="hidePokemonList" :setUpdatePokemonName="setUpdatePokemonName" :setUpdatePokemonType="setUpdatePokemonType" :setUpdatePokemonPower="setUpdatePokemonPower" :setDeletePokemonName="setDeletePokemonName"/>
  </div>
</template>

<script>
import testData from '../testData'
import PokemonCard from './PokemonCard.vue'

export default {
    props: ['openUpdateModal','openDeleteModal','hidePokemonList','setUpdatePokemonName','setUpdatePokemonType','setUpdatePokemonPower','setDeletePokemonName'],
    data() {
        return {
            pokemonList: testData
        };
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