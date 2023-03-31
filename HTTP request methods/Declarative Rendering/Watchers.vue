Czasami może być konieczne reaktywne wykonanie „skutków ubocznych” - na przykład zalogowanie numeru do konsoli, gdy się zmieni. Możemy to osiągnąć dzięki obserwatorom:

import { ref, watch } from 'vue'

const count = ref(0)

watch(count, (newCount) => {
  // yes, console.log() is a side effect
  console.log(`new count is: ${newCount}`)
})

watch()może bezpośrednio oglądać ref, a wywołanie zwrotne jest uruchamiane za każdym razem, gdy countzmienia się wartość ' s . 
watch()może również oglądać inne typy źródeł danych

<script setup>
import { ref, watch } from 'vue'

const todoId = ref(1)
const todoData = ref(null)

async function fetchData() {
  todoData.value = null
  const res = await fetch(
    `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
  )
  todoData.value = await res.json()
}

fetchData()

watch(todoId, fetchData)
</script>

<template>
  <p>Todo id: {{ todoId }}</p>
  <button @click="todoId++">Fetch next todo</button>
  <p v-if="!todoData">Loading...</p>
  <pre v-else>{{ todoData }}</pre>
</template>