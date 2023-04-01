Aby powiązać atrybut z wartością dynamiczną, używamy dyrektywy v-bind

<div v-bind:id="dynamicId"></div>

Dyrektywa to specjalny atrybut, który zaczyna się od przedrostkav- . 
Są częścią składni szablonów Vue. 
Podobnie jak w przypadku interpolacji tekstu, wartości dyrektywy są wyrażeniami JavaScript, które mają dostęp do stanu komponentu. 

Część po dwukropku ( :id) jest „argumentem” dyrektywy. 
Tutaj atrybut elementu idzostanie zsynchronizowany z dynamicIdwłaściwością ze stanu komponentu.

Ponieważ v-bindjest używany tak często, ma dedykowaną skróconą składnię:

<div :id="dynamicId"></div>


example:
<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
</script>

<template>
  <h1 :class="titleClass">Make me red</h1>
</template>

<style>
.title {
  color: red;
}
</style>