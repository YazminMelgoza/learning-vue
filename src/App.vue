<script setup>
import { ref } from 'vue'

const contador = ref(0)

function incrementar() {
  contador.value++
}
</script>

<template>
  <h2 :class="contador >= 20 ? 'red' : ''">Contador reactivo: {{ contador }}</h2>
  <button @click="incrementar">Aumentar</button>
  <button @click="incrementar()">Decrementar</button>
</template>

<style>
.red {
  color: red;
}
</style>
