<template>
  <!-- eslint-disable -->
  <div class="searchBarDiv">
      <button id="name-btn" :class="{ activeSearch: activeSearchField === 'name' }" @click="toggleActiveSearchToName">NAME</button>
      <button id="type-btn" :class="{ activeSearch: activeSearchField === 'type' }" @click="toggleActiveSearchToType">TYPE</button>
      <br>
      <input type="text" name="searchBar" id="pokemonSearchBar" :placeholder="activeSearchField==='name' ? nameSearchPlaceHolder : typeSearchPlaceHolder">
      <button class="close">CLOSE</button>
  </div>
</template>

<script>
export default {
    data(){
        return{
            nameSearchPlaceHolder: "Enter Pokemon Name...",
            typeSearchPlaceHolder: "Enter Pokemon Type...",
            activeSearchField: "name"
        }
    },
    methods : {
        toggleActiveSearchToName() {
            this.activeSearchField = 'name';
        },
        toggleActiveSearchToType() {
            this.activeSearchField = 'type';
        }
    }
}
</script>

<style scoped>
    .searchBarDiv{
        margin: 10px;
    }
    button{
        margin: 10px 0;
        height: 40px;
        padding: 10px;
        border-radius: 5px;
        cursor: pointer;
    }
    #name-btn{
        border-top-right-radius: 0;
        border-bottom-right-radius: 0;
        border-right-width: 1px;
    }
    #type-btn{
        border-top-left-radius: 0;
        border-bottom-left-radius: 0;
        border-left-width: 1px;
    }
    input{
        height: 40px;
        width: 50%;
        font-size: 20px;
        padding: 8px;
    }
    button.activeSearch{
        background-color: rgb(251, 184, 126);
    }

    .close{
        background-color: #eb3d3d;
        color: white;
        padding: 10px;
        width: fit-content;
        border-radius: 5px;
        margin: 10px auto;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 12px;
        cursor: pointer;
        font-weight: normal;
        border: 0;
    }
</style>