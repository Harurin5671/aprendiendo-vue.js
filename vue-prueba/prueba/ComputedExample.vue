<script lang="ts">
// computed option
// import { defineComponent } from 'vue'
// export default defineComponent({
//   name: 'ComputedExample',
//   data() {
//     return{
//       message: ''
//     }
//   },
//   computed: {
//     reverse():string {
//       return this.message.split('').reverse().join('')
//     }
//   }
// })

//computed composition
import { defineComponent, type Ref, ref, computed } from 'vue'
export default defineComponent({
  name: 'ComputedExample',
  setup() {
    let message = ref('')
    const reverse = computed(() => message.value.split('').reverse().join(''))
    return { message, reverse }
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