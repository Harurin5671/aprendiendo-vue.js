<script lang='ts' setup>
  let age:number = 15;
</script>

<template>
  <h1 v-if="age < 18">Soy menor de edad</h1>
  <h1 v-else>Soy mayor de edad</h1>
</template>

<style scoped>
  
</style>


/* 
el v-if/ v-else no pinta el nodo en el doom
el v-show si lo pinta pero le pone un display:none mediante CSS y asi evita que se muestre pero si esta en el doom
*/