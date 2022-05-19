<template>
  <!-- eslint-disable -->
  <div class="addModal">
    <h2>Add a Pokemon</h2>
    <div class="addModalContent">
      <label for="name">Pokemon Name</label><br>
      <input type="text" name="name" placeholder="Enter Pokemon Name"><br>
      <label for="type">Pokemon Type</label><br>
      <select name="type">
        <option value="grass">Grass</option>
        <option value="fire">Fire</option>
        <option value="water">Water</option>
        <option value="rock">Rock</option>
      </select><br>
      <label for="power">Pokemon Power</label><br>
      <input type="number" name="power" placeholder="Enter pokemon power">
    </div>
    <button>Add Pokemon</button>
    <button class="close" @click="closeAddModal">X</button>
  </div>
</template>

<script>
export default {
  props: ['closeAddModal']
}
</script>

<style scoped>
  h2{
    text-align: center;
  }
  .addModal{
    padding: 16px;
    border-radius: 12px;
    width: 40%;
    background-color: rgb(195, 194, 194);
    margin: 10px auto;
    text-align: left;
    position: relative;
  }
  .addModalContent{
    margin-left: 20px;
  }
  label{
    color: black;
    font-size: 16px;
  }

  input{
    height: 20px;
    width: 90%;
    padding: 6px;
    margin: 5px 0 10px 0;
  }

  select{
    height: 36px;
    width: 93%;
    margin: 5px 0 10px 0;
  }

  button{
    display: block;
    margin: 10px auto;
    height: 40px;
    width: 92%;
    border: 0;
    border-radius: 5px;
    color: white;
    background-color: rgb(72, 197, 61);
    cursor: pointer;
    opacity: 0.9;
    transition: all 0.5s ease;
  }

  button:hover{
      opacity: 1;
      transform: scale(1.05);
  }

  .close{
    position: absolute;
    background-color: #f44c4c;
    height: 30px;
    width: 30px;
    top: 5%;
    right: 5%;
  }
  
</style>