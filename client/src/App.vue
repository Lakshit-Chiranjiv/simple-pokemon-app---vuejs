<script setup>
  import Header from './components/Header.vue';
  import OpsPanel from './components/OpsPanel.vue';
  import SearchBar from './components/SearchBar.vue';
  import AddModal from './components/AddModal.vue';
  import UpdateModal from './components/UpdateModal.vue';
  import DeleteModal from './components/DeleteModal.vue';
  import PokemonCard from './components/PokemonCard.vue';
  import RandomModal from './components/RandomModal.vue';
  import { ref } from 'vue';

  const openOpsPanel = ref(false);
  const searchBarState = ref(false);
  const activeSearchField = ref('name');
  const addModalOpenState = ref(false);
  const updateModalOpenState = ref(false);
  const deleteModalOpenState = ref(false);
  const randomModalOpenState = ref(false);

  const toggleOpsPanel = () => {
    openOpsPanel.value = !openOpsPanel.value;
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
</script>

<template>
<!-- eslint-disable -->
  <Header :toggleOpsPanel="toggleOpsPanel"/>
  <OpsPanel v-show="openOpsPanel" :toggleOpsPanel="toggleOpsPanel" :openSearchBar="openSearchBar" 
  @name-search-btn-clicked="toggleActiveSearchToName" @type-search-btn-clicked="toggleActiveSearchToType" :openAddModal="openAddModal" :openRandomModal="openRandomModal"/>
  <SearchBar v-if="searchBarState" :closeSearchBar="closeSearchBar" :activeSearchField="activeSearchField" :toggleActiveSearchToName="toggleActiveSearchToName" :toggleActiveSearchToType="toggleActiveSearchToType"/>
  <AddModal v-if="addModalOpenState" :closeAddModal="closeAddModal"/>
  <UpdateModal v-if="updateModalOpenState"/>
  <DeleteModal v-show="deleteModalOpenState"/>
  <RandomModal v-show="randomModalOpenState" :closeRandomModal="closeRandomModal"/>
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
  /* background-color: rgb(56, 56, 56); */
}

button{
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.4px;
}
</style>
