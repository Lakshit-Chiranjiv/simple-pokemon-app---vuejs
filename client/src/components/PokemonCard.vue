<template>
  <div class="card">
      <div class="details">
        <div class="nameDetails">
            <h3>Pikachu</h3>
            <h5>Electric</h5>
        </div>
        <div class="powerDetails">
            <p>82</p>
        </div>
      </div>
      <div class="cardBtns">
        <button><img src="./../assets/pencil.png" alt="edit"></button>
        <button><img src="./../assets/delete.png" alt="delete"></button>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

    .card{
        width: 30%;
        background-color: #2d2d2d;
        margin: 10px auto;
        color: white;
        padding: 16px 4px;
        border-radius: 16px;
    }

    h3{
        font-size: 24px;
    }

    h3,h5{
        font-weight: 200;
        margin: 8px;
    }
    .details{
        display: flex;
        justify-content: space-around;
        align-items: center;
        text-align: left;
    }

    .powerDetails{
        font-size: 36px;
        font-weight: 100;
    }

    img{
    width: 20px;
    cursor: pointer;
    }
    .cardBtns{
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    button{
        height: 40px;
        width: 20%;
        border: 0;
        border-radius: 5px;
        background-color: #ffffff;
        cursor: pointer;
        opacity: 0.8;
        transition: all 0.5s ease;
    }

    button:hover{
        opacity: 1;
        transform: scale(1.05);
    }
</style>