<template >
  <form>
    <input type="text" v-model="inputText" />
    <input type="checkbox" v-model="agree"/>Acepto los términos
    <select v-model="country">
      <option value="Spain">Spain</option>
      <option value="UK">Uk</option>
      <option value="France">France</option>
    </select>
  </form>
  <h3>{{ inputText }}</h3>
</template>

<script lang="ts" setup>
import { type Ref, ref } from 'vue'
let inputText:Ref<string> = ref('')
let agree = ref(true)
let country = ref('Spain')
</script>

<style scoped>
  
</style>