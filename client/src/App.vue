<script setup>
  import Header from './components/Header.vue';
  import OpsPanel from './components/OpsPanel.vue';
  import SearchBar from './components/SearchBar.vue';
  import AddModal from './components/AddModal.vue';
  import UpdateModal from './components/UpdateModal.vue';
  import DeleteModal from './components/DeleteModal.vue';
  import PokemonCard from './components/PokemonCard.vue';
  import RandomModal from './components/RandomModal.vue';
  import PokemonDisplay from './components/PokemonDisplay.vue';
  import { ref } from 'vue';

  const openOpsPanel = ref(false);
  const searchBarState = ref(false);
  const activeSearchField = ref('name');
  const addModalOpenState = ref(false);
  const updateModalOpenState = ref(false);
  const deleteModalOpenState = ref(false);
  const randomModalOpenState = ref(false);
  const pokemonListShowState = ref(true);

  const updatePokemonName = ref('')
  const updatePokemonType = ref('')
  const updatePokemonPower = ref(0)

  const searchText = ref('')

  const deletePokemonName = ref('')

  const setUpdatePokemonName = (nameToSet) => {
    updatePokemonName.value = nameToSet;
  }
  const setUpdatePokemonType = (typeToSet) => {
    updatePokemonType.value = typeToSet;
  }
  const setUpdatePokemonPower = (powerToSet) => {
    updatePokemonPower.value = powerToSet;
  }

  const setDeletePokemonName = (nameToSet) => {
    deletePokemonName.value = nameToSet;
  }

  const toggleOpsPanel = () => {
    openOpsPanel.value = !openOpsPanel.value;
  }

  const closeOpsPanel = () => {
    openOpsPanel.value = false;
  }

  const openSearchBar = () => {
    searchBarState.value = true;
  }

  const closeSearchBar = () => {
    searchBarState.value = false;
  }

  const toggleActiveSearchToName = () => {
    activeSearchField.value = 'name';
  }
  const toggleActiveSearchToType = () => {
    activeSearchField.value = 'type';
  }

  const openAddModal = () => {
    addModalOpenState.value = true;
  }
  const closeAddModal = () => {
    addModalOpenState.value = false;
  }

  const openUpdateModal = () => {
    updateModalOpenState.value = true;
  }
  const closeUpdateModal = () => {
    updateModalOpenState.value = false;
  }
  
  const openDeleteModal = () => {
    deleteModalOpenState.value = true;
  }
  const closeDeleteModal = () => {
    deleteModalOpenState.value = false;
  }

  const openRandomModal = () => {
    randomModalOpenState.value = true;
  }
  const closeRandomModal = () => {
    randomModalOpenState.value = false;
  }

  const showPokemonList = () => {
    pokemonListShowState.value = true;
  }
  const hidePokemonList = () => {
    pokemonListShowState.value = false;
  }

  const setAllStatesToDefault = () => {
    closeAddModal();
    closeUpdateModal();
    closeSearchBar();
    closeRandomModal();
    closeDeleteModal();
    showPokemonList();
  }
</script>

<template>
<!-- eslint-disable -->
  <Header :openOpsPanel="openOpsPanel" :toggleOpsPanel="toggleOpsPanel" :setAllStatesToDefault="setAllStatesToDefault"/>

  <OpsPanel v-show="openOpsPanel" :toggleOpsPanel="toggleOpsPanel" :openSearchBar="openSearchBar" 
  @name-search-btn-clicked="toggleActiveSearchToName" @type-search-btn-clicked="toggleActiveSearchToType" :openAddModal="openAddModal" :openRandomModal="openRandomModal" :hidePokemonList="hidePokemonList"/>

  <SearchBar v-if="searchBarState" :closeSearchBar="closeSearchBar" :activeSearchField="activeSearchField" :toggleActiveSearchToName="toggleActiveSearchToName" :toggleActiveSearchToType="toggleActiveSearchToType" :showPokemonList="showPokemonList" :searchText="searchText"/>

  <AddModal v-if="addModalOpenState" :closeAddModal="closeAddModal" :showPokemonList="showPokemonList"/>

  <UpdateModal v-if="updateModalOpenState" :closeUpdateModal="closeUpdateModal" :showPokemonList="showPokemonList" :updatePokemonName="updatePokemonName" :updatePokemonType="updatePokemonType" :updatePokemonPower="updatePokemonPower"/>

  <DeleteModal v-show="deleteModalOpenState" :closeDeleteModal="closeDeleteModal" :showPokemonList="showPokemonList" :deletePokemonName="deletePokemonName"/>

  <RandomModal v-show="randomModalOpenState" :closeRandomModal="closeRandomModal" :showPokemonList="showPokemonList"/>

  <PokemonDisplay v-if="pokemonListShowState" :openUpdateModal="openUpdateModal" :openDeleteModal="openDeleteModal" :hidePokemonList="hidePokemonList" :setUpdatePokemonName="setUpdatePokemonName" :setUpdatePokemonType="setUpdatePokemonType" :setUpdatePokemonPower="setUpdatePokemonPower" :setDeletePokemonName="setDeletePokemonName" :closeOpsPanel="closeOpsPanel"/>


  
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
  /* background-color: rgb(56, 56, 56); */
}

button{
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.4px;
}
</style>
