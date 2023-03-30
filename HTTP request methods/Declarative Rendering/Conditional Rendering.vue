Możemy użyć v-ifdyrektywy do warunkowego renderowania elementu:

h1 v-if="awesome">Vue is awesome!</h1>

Możemy również użyć v-elsei v-else-ifdo oznaczenia innych gałęzi warunku:

<h1 v-if="awesome">Vue is awesome!</h1>
<h1 v-else>Oh no 😢</h1>


np.
<script setup>
import { ref } from 'vue'

const awesome = ref(true)

function toggle() {
  awesome.value = !awesome.value
}
</script>

<template>
  <button @click="toggle">toggle</button>
  <h1 v-if="awesome">Vue is awesome!</h1>
  <h1 v-else>Oh no 😢</h1>
</template>