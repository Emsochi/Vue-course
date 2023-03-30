Używając v-bindi v-onrazem, możemy tworzyć dwukierunkowe powiązania na elementach wejściowych formularza:

<input :value="text" @input="onInput">

function onInput(e) {
  text.value = e.target.value
}

np.
<script setup>
import { ref } from 'vue'

const text = ref('')

function onInput(e) {
  text.value = e.target.value
}
</script>

<template>
  <input :value="text" @input="onInput" placeholder="Type here">
  <p>{{ text }}</p>
</template>
