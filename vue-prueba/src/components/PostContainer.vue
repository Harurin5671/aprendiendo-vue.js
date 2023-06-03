<script lang="ts" setup>
import PostCard from './PostCard.vue'
</script>

<template>
  <div class="post-container">
    <PostCard />
    <PostCard />
    <PostCard />
    <PostCard />
  </div>
</template>

<style scoped>
.post-container {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}
</style>