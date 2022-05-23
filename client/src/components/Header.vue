<template>
<!-- eslint-disable -->
<div class="head">
  <h1>Pokemon App</h1>
  <div class="panelBtn" @click="handleOpsBtnClick">
    <a href="#">+</a>
  </div>
</div>
</template>

<script setup>
  const props = defineProps(['openOpsPanel','toggleOpsPanel','setAllStatesToDefault'])

  const handleOpsBtnClick = () => {
    if(props.openOpsPanel === false)
      props.setAllStatesToDefault();
    props.toggleOpsPanel();
  }
</script>

<style scoped>
.head{
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}
h1{
    font-size: 72px;
}
.panelBtn{
  border: 5px solid #00a900;
  padding: 4px;
  height: 40px;
  width: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
}
a{
  text-decoration: none;
  font-size: 72px;
  color: #00a900;
}

</style>