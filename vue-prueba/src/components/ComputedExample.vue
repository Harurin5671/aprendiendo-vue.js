<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'ComputedExample',
  data() {
    return{
      message: ''
    }
  },
  computed: {
    reverse():string {
      return this.message.split('').reverse().join('')
    }
  }
})
</script>

<template>
  <div>
    <input type="text" v-model="message" />
    <h2>{{ message }}</h2>
    <h2>{{ reverse }}</h2>
  </div>
</template>

<style scoped>
</style>