<template>
  <!-- eslint-disable -->
  <!-- <button id="bt" @click="clickHandle">Open</button> -->
  <div ref="panel">
      <a href="#"><button :style="{color:'white', backgroundColor: 'green'}">Add Pokemon</button></a>
      <a href="#"><button :style="{color:'white', backgroundColor: 'orange'}">Search Pokemon Name</button></a>
      <a href="#"><button :style="{color:'white', backgroundColor: 'blue'}">Search Pokemon Type</button></a>
      <a href="#"><button :style="{color:'white', backgroundColor: 'purple'}">Generate Random Pokemon</button></a>
  </div>
</template>

<script>

export default {
    methods: {
        clickHandle() {
            console.log(45,this.$refs.panel.style.bottom);
            // this.$refs.panel.style.bottom = '50px';
            if(!this.$refs.panel.style.bottom || this.$refs.panel.style.bottom=='0px'){
                this.$refs.panel.style.bottom = '-190px';
            }
            else{
                this.$refs.panel.style.bottom = '0px';
            }
                
            
        }
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
}
button{
    height: 40px;
    padding: 10px;
    border-radius: 5px;
    border: 0;
    cursor: pointer;
    margin: 10px 15px;
}
</style>