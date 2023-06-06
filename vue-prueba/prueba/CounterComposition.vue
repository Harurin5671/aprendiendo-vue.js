// Sin usar setup
<!-- <script lang="ts">
import { defineComponent, type Ref, ref } from 'vue'
export default defineComponent({
  name: 'CounterComposition',
  setup() {
    let counter:Ref = ref(0)
    const addCounter = ():void => {
      counter.value++
    }
    return { counter, addCounter }
  }
})
</script> -->

<script lang="ts" setup>
import { type Ref, ref } from 'vue'
let counter:Ref = ref(0)
const addCounter = ():void => {
  counter.value++
}
</script>

<template>
  <h3>{{ counter }}</h3>
  <button @click="addCounter">Incrementar</button>
</template>

<style scoped></style>


/* 
formas de trabajo aquí
export default {
  name: "component",
  props: { ... },        // Props
  setup() {
    //init logic, lifecycle hooks, etc...
    return {
      // data, methods, computed, etc...
    }
  }
}
*/