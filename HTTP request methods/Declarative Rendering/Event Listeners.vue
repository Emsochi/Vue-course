Możemy nasłuchiwać zdarzeń DOM za pomocą v-ondyrektywy:

<button v-on:click="increment">{{ count }}</button>

Ze względu na częste użycie v-onma również skróconą składnię:

<button @click="increment">{{ count }}</button>

np.

<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}
</script>

<template>
  <button @click = "increment">{{count}}</button>
</template>