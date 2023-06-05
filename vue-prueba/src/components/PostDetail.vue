<script lang="ts">
// sin usar setup
import { defineComponent, ref, type Ref } from 'vue';
export default defineComponent({
  name: 'PostDetail',
  props: {
    title: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: false,
      default: 'No hay contenido'
    }
  },
  emits: ['sayHi'],
  setup(props, { emit }) {
    const handleClick = () => {
      emit('sayHi', message.value)
    }
    let message:Ref<string> = ref('')
    return { props, handleClick, message }
  }
})

</script>

<template>
  <div class="post">
    <h3>{{ props.title }}</h3>
    <p>{{ props.content }}</p>
    <input type="text" v-model="message" />
    <button @click="handleClick" >Di hola</button>
  </div>
</template>

<style scoped>
.post {
  width: 300px;
  height: 200px;
  background-color: #a9f;
  border-radius: 10px;
  margin: 10px;
  padding: 10px;
}
</style>
