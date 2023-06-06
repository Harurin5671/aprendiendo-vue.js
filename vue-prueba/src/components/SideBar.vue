<script lang="ts" setup>
import DrawerWork from './DrawerWork.vue'
</script>

<template>
  <div class="container_sidebar">
    <div class="container-actions">
      <button class="btn add">
        <i class="bi bi-plus-square"></i>
      </button>
      <button class="btn layers">
        <i class="bi bi-layers"></i>
      </button>
      <button class="btn css">
        <i class="bi bi-filetype-css"></i>
      </button>
      <button class="btn folder"><i class="bi bi-folder"></i></button>
    </div>
    <dir class="div_vació"></dir>
    <div class="container-actions-bot">
      <button class="btn"><i class="bi bi-file-earmark-text"></i></button>
      <button class="btn"><i class="bi bi-discord"></i></button>
      <button class="btn"><i class="bi bi-question-circle"></i></button>
    </div>
  </div>
  <DrawerWork />
</template>

<style scoped>
.container_sidebar {
  text-align: center;
  width: 3vw;
  height: 94.8vh;
  border-right: 1px solid #000;
}

.div_vació {
  height:55vh;
}

.container-actions {
  display: flex;
  flex-direction: column;
}

.container-actions-bot {
  display: flex;
  flex-direction: column;
  position: relative;
  top: 3.2rem;
}

.btn {
  background-color: transparent;
  border: 0;
  margin: 10px 0 10px 0;
}

.bi {
  font-size: 23px;
  height: 100%;
}
</style>
