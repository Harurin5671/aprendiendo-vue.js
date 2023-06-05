<script lang="ts" setup>
import { onMounted, onUpdated } from 'vue'

onMounted(() => console.log('mounted'))

onUpdated(() => console.log('updated'))
</script>

<template>
  <div>Hola Mundo</div>
</template>

<style scoped></style>
