<template>
<div>
  <Principal />
  <Cursos />
  <Sobre />
</div>
</template>

<script lang="ts">
import Vue from 'vue'
import Cursos from '~/components/Cursos.vue'
import Principal from '~/components/Principal.vue'

export default Vue.extend({
  components: { Principal, Cursos },})
</script>
