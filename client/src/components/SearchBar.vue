<template>
  <!-- eslint-disable -->
  <div class="searchBarDiv">
      <button id="name-btn">NAME</button>
      <button id="type-btn">TYPE</button>
      <br>
      <input type="text" name="searchBar" id="pokemonSearchBar" :placeholder="nameSearchPlaceHolder">
  </div>
</template>

<script>
export default {
    data(){
        return{
            nameSearchPlaceHolder : "Enter Pokemon Name...",
            typeSearchPlaceHolder : "Enter Pokemon Type..."
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
</style>