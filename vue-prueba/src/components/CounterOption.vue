<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  name: 'CounterOption',
  data() {
    let counter = 0
    return { counter }
  },
  methods: {
    addCounter() {
      this.counter++
    }
  }
})
</script>

<template>
  <h3>
    {{ counter }}
  </h3>
  <button @click="addCounter">Incrementar</button>
</template>

<style scoped></style>

/* 
formas de trabajo aquí
export default {
  name: "componentName",
  props: { ... },        // Props
  data() { ... },        // Data Variables
  computed: { ... },     // Computed Props
  methods: { ... }       // Functions
  mounted() { ... }      // Mounted hook (lifecycle)
}


*/