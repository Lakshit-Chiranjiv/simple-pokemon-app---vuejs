<script setup>
import Header from './components/Header.vue';
import OpsPanel from './components/OpsPanel.vue';
import SearchBar from './components/SearchBar.vue';
import AddModal from './components/AddModal.vue';
import UpdateModal from './components/UpdateModal.vue';
import DeleteModal from './components/DeleteModal.vue';
import PokemonCard from './components/PokemonCard.vue';
import RandomModal from './components/RandomModal.vue';

</script>

<template>
<!-- eslint-disable -->
  <Header/>
  <OpsPanel/>
  <SearchBar/>
  <AddModal/>
  <UpdateModal/>
  <DeleteModal/>
  <RandomModal/>
  <PokemonCard/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
}

button{
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.4px;
}
</style>
