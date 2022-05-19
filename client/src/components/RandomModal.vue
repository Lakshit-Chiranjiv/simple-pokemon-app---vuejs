<template>
  <div class="randModal">
    <h2>Random Pokemon</h2>
    <h3>Pikachu</h3>
    <div class="randModalBtn">
        <button>GENERATE ANOTHER</button>
        <button class="close">X</button>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  h2,h3{
    text-align: center;
  }
  .randModal{
    padding: 16px;
    border-radius: 12px;
    width: 40%;
    background-color: #c3c2c2;
    margin: 10px auto;
    position: relative;
  }
  .randModalBtns{
    margin: 10px auto;
  }

  button{
    height: 40px;
    width: 90%;
    border: 0;
    border-radius: 5px;
    color: #ffffff;
    background-color: #d65aff;
    cursor: pointer;
    opacity: 0.8;
    transition: all 0.5s ease;
    margin-bottom: 10px;
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