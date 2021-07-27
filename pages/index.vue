<template>
<div>
  <Principal />
  <Tutorial />
</div>
</template>

<script lang="ts">
import Vue from 'vue'
import Principal from '~/components/Principal.vue'

export default Vue.extend({
  components: { Principal },})
</script>
