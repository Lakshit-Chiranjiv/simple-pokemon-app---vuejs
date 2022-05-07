<script setup>
import Header from './components/Header.vue';
import OpsPanel from './components/OpsPanel.vue';
import SearchBar from './components/SearchBar.vue';
import AddModal from './components/AddModal.vue';
import UpdateModal from './components/UpdateModal.vue';

</script>

<template>
<!-- eslint-disable -->
  <Header/>
  <OpsPanel/>
  <SearchBar/>
  <AddModal/>
  <UpdateModal/>
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
</style>
