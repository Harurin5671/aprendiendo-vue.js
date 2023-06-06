<script lang="ts" setup>
import { type Ref, ref } from 'vue'
interface ICountry {
  code: string,
  name: string
}

let countries:Ref<Array<ICountry>> = ref([
  {
    code: 'es',
    name: 'Spain'
  },
  {
    code: 'en',
    name: 'Uk'
  },
  {
    code: 'fr',
    name: 'France'
  },
  {
    code: 'it',
    name: 'Italy'
  },
  {
    code: 'pt',
    name: 'Portugal'
  },

])
</script>

<template>
  <ul>
    <li v-for="country in countries" :key="country.code">{{ country.name }}</li>
  </ul>
</template>

<style scoped>

</style>