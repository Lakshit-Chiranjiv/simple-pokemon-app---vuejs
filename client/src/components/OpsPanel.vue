<template>
  <!-- eslint-disable -->
  <!-- <button id="bt" @click="clickHandle">Open</button> -->
  <div ref="panel">
      <a href="#"><button :style="{color:'white', backgroundColor: 'green'}" @click="handleAddBtn">Add Pokemon</button></a>
      <a href="#"><button :style="{color:'white', backgroundColor: 'orange'}" @click="handleSearchNameBtn">Search Pokemon Name</button></a>
      <a href="#"><button :style="{color:'white', backgroundColor: 'blue'}" @click="handleSearchTypeBtn">Search Pokemon Type</button></a>
      <a href="#"><button :style="{color:'white', backgroundColor: 'purple'}" @click="handleGenRandomBtn">Generate Random Pokemon</button></a>
  </div>
</template>

<script>

export default {
    props: ['toggleOpsPanel','openSearchBar','openAddModal','openRandomModal','hidePokemonList'],
    emits: ["nameSearchBtnClicked","typeSearchBtnClicked"],
    methods: {
        handleAddBtn() {
            this.toggleOpsPanel();
            this.openAddModal();
            this.hidePokemonList();
        },
        handleSearchNameBtn() {
            this.$emit("nameSearchBtnClicked");
            this.openSearchBar();
            this.toggleOpsPanel();
            this.hidePokemonList();
        },
        handleSearchTypeBtn() {
            this.$emit("typeSearchBtnClicked");
            this.openSearchBar();
            this.toggleOpsPanel();
            this.hidePokemonList();
        },
        handleGenRandomBtn() {
            this.toggleOpsPanel();
            this.openRandomModal();
            this.hidePokemonList();
        },


        // clickHandle() {
        //     console.log(45,this.$refs.panel.style.bottom);
        //     // this.$refs.panel.style.bottom = '50px';
        //     if(!this.$refs.panel.style.bottom || this.$refs.panel.style.bottom=='0px'){
        //         this.$refs.panel.style.bottom = '-190px';
        //     }
        //     else{
        //         this.$refs.panel.style.bottom = '0px';
        //     }
        // }
    }
}
</script>

<style scoped>
/* .bottomPanel{
    position: absolute;
    background-color: #e75555;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    gap: 15px;
    height: 170px;
    width: 97%;
    bottom: 0;
    transition: all 0.6s;
} */
    a{
        text-decoration: none;
        margin: 0 15px;
    }

    button{
        margin: 10px auto;
        height: 40px;
        width: 20%;
        padding: 10px;
        border: 0;
        border-radius: 5px;
        color: white;
        cursor: pointer;
        opacity: 0.9;
        transition: all 0.5s ease;
    }

    button:hover{
        opacity: 1;
        transform: scale(1.05);
    }
</style>