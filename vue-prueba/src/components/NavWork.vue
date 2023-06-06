<script lang="ts" setup>
import ActionWork from './ActionWork.vue'
const handleClick = () => {
  console.log('click')
}
</script>

<template>
  <div class="nav">
    <button @click="handleClick" class="btn"><i class="bi bi-list"></i></button>
    <div class="container_user">
      <span class="content">Designer</span>
      <span class="content">Developer</span>
    </div>
    <div class="project_container">
      <span class="project-content">Titulo</span>
      <div class="container_public">
        <span class="project-content_public"><i class="bi bi-globe"></i>PUBLIC</span>
      </div>
    </div>
    <ActionWork />
  </div>
</template>

<style scoped>
.nav {
  height: 50px;
  width: 100%;
  /* border: 1px solid black; */
  display: inline-flex;
  justify-content: space-between;
  text-align: center;
  align-items: center;
  border-bottom: 1px solid rgba(0, 0, 0 , .2);
}

.container_user {
  background-color: rgb(150, 150, 150);
  margin-top: 1px;
  width: 220px;
  height: 35px;
  display: flex;
  border-radius: 15px;
  justify-content: space-evenly;
  position: relative;
  right: 180px;
  align-items: center;
}

.content {
  background-color: rgb(180, 180, 180);
  height: 25px;
  width: 100px;
  margin: 0 20px 0 20px;
  display: inline-flex;
  /* text-align: center;*/
  align-items: center;
  justify-content: center;
  border-radius: 10px;
}

.project_container {
  /* border: 2px solid #72f; */
  display: flex;
  position: relative;
  right: 100px;
  width: 20%;
  justify-content: center;
  align-items: center;
  height: 35px;
}

.project-content {
  margin: 0 10px 0 10px;
  font-weight: 600;
}
.project-content_public {
  /* margin: 0 10px 0 10px; */
  color: #fff;
  padding: 2px 4px;
}

.btn {
  position: relative;
  left: .9rem;
  background-color: transparent;
  border: 0;
}
.container_public {
  display: flex;
  /* margin: 0 10px 0 10px; */
  align-items: center;
  background-color: #f8681c;
  height: 25px;
  border-radius: 9px;
}

.bi {
  font-size: 23px;
}

.bi-globe {
  font-size: 15px;
  font-weight: 600;
  margin-right: 5px;
}</style>