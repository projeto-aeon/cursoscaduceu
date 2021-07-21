<template>
  <div class="container">
    <h1 v-if="error.statusCode === 404">Página não encontrada</h1>
    <h1 v-else>Erro</h1>
    <NuxtLink to="/">Início</NuxtLink>
  </div>
</template>

<script>
export default {
  props: ['error']
}
</script>
