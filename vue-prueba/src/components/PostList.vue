<script lang="ts" setup>
import PostDetail from './PostDetail.vue'

interface Post {
  title: string,
  content: string
}

let info:Array<Post> = [
  {
    title: 'este es el post 1',
    content: 'texto de ejemplo1'
  },
  {
    title: 'este es el post 2',
    content: 'texto de ejemplo2'
  },
  {
    title: 'este es el post 3',
    content: 'texto de ejemplo3'
  },
  {
    title: 'este es el post 4',
    content: 'texto de ejemplo4'
  },
  {
    title: 'este es el post 5',
    content: 'texto de ejemplo5'
  }
]

function showAlert(msg:string) {
  alert(msg)
}
</script>

<template>
  <div class="container">
    <PostDetail v-for="elm in info" :key="elm.title" :title="elm.title" :content="elm.content" @sayHi="showAlert" />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>
