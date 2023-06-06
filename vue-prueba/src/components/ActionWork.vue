<script lang="ts" setup>
import image from '../../public/77626612.jpeg'
</script>

<template>
  <div class="actions_container">
    <div class="perfil_container">
      <img class="img_perfil" :src="image" alt="imagen-perfil" />
      <button class="perfil_btn">Share</button>
    </div>
    <div class="actions">
      <button class="btn"><i class="bi bi-code-slash"></i></button>
      <button class="btn"><i class="bi bi-box-arrow-down"></i></button>
      <button class="btn"><i class="bi bi-eye"></i></button>
    </div>
    <div class="actions_finish">
      <button class="finish publish">Publish</button>
      <button class="finish upgrade">Upgrade</button>
    </div>
  </div>
</template>

<style scoped>
.actions_container {
  /* border: 2px solid red; */
  display: flex;
  flex-wrap: wrap;
  text-align: center;
  justify-content: space-around;
  align-items: center;
  width: 400px;
}
.perfil_container {
  display: flex;
  align-items: center;
  position: relative;
  /* border: 2px solid red; */
  /* left: 100px; */
}
.img_perfil {
  width: 35px;
  height: 35px;
  border-radius: 50%;
  margin: 0 15px 0 0;
}
.perfil_btn {
 border: 1px solid rgb(100, 100, 100);
 background-color: rgb(180, 180, 180);
 border-radius: 4px;
 padding: 4px;
}
.actions {
  border-left:1px solid rgb(0, 0, 0);
  border-right: 1px solid rgb(0, 0, 0);
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 100px;
  height: 50px;
}

.btn {
  background-color: transparent;
  border: 0;
  /* border: 1px solid red; */
}
.actions_finish {
  display: flex;
  align-items: center;
  justify-content: space-between;
  /* border: 2px solid #563; */
  height: 100%;
}
.actions_finish button {
  margin: 10px;
}
.bi {
  font-size: 23px;
  margin: 0 4px 0 4px;
}
.finish {
  border-radius: 6px;
  height: 30px;
  padding: 5px;
  cursor: pointer;
}
.publish {
  border: 1px solid rgb(195, 195, 195)
}
.upgrade {
  background-color: #0f8fff;
  border: #0f8299;
  color: #fff;
}
</style>