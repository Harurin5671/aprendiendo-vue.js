<script lang="ts">
/*
 ** Composition 
 import { defineComponent } from 'vue'
 export default defineComponent({
   name: 'ClassBind',
   setup() {
     let hasError = false
     return { hasError }
   }
 })
 */

 // usando setup
// let hasError = false
/**
 **Option 
 import { defineComponent } from 'vue';
 export default defineComponent({
   name: 'ClassBind',
   data() {
     return {
       hasError: true
     }
   }
 })
*/

//usando setup
// import { type Ref, ref } from 'vue'
// let c = ref('#fff')
// let changeColor = () => {
//   c.value = '#000'
// }

//option
import { defineComponent } from 'vue';
export default defineComponent({
  name: 'ClassBind',
  data() {
    return {
      c: '#fff'
    }
  },
  methods: {
    changeColor() {
      this.c = '#000'
    }
  }
})
</script>

<template>
  <p v-bind:style="{
    backgroundColor : '#c7f', color: c
  }">El mensaje se ha enviado satisfactoriamente.</p>
  <button @click="changeColor">Cambiar color</button>
</template>

<style>
.danger {
  color: #f00;
}
</style>


// v-bind su abreviatura es :key, class y demás
// v-on su abreviatura es @click u y demás