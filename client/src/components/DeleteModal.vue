<template>
  <div class="delModal">
      <h2>Delete Pokemon??</h2>
      <h3>Pikachu</h3>
      <div class="delModalBtns">
          <button>CANCEL</button>
          <button>DELETE</button>
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
  .delModal{
    padding: 16px;
    border-radius: 12px;
    width: 40%;
    background-color: #c3c2c2;
    margin: 10px auto;
  }
  .delModalBtns{
    display: flex;
    gap: 10px;
    margin: 10px auto;
    justify-content: center;
    align-items: center;
  }

  button{
    height: 40px;
    width: 40%;
    border: 0;
    border-radius: 5px;
    color: #ffffff;
    cursor: pointer;
    opacity: 0.8;
    transition: all 0.5s ease;
  }

  button:hover{
      opacity: 1;
      transform: scale(1.05);
  }

  button:nth-child(1){
      background-color: #63a2fb;
  }

  button:nth-child(2){
      background-color: #fb6363;
  }

</style>