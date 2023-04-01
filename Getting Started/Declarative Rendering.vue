// używając składni szablonu, która rozszerza HTML, możemy opisać, jak HTML powinien wyglądać na podstawie stanu JavaScript. 
Kiedy zmienia się stan, kod HTML aktualizuje się automatycznie.

// Stany, które po zmianie mogą wyzwalać aktualizacje, są uważane za reaktywne .

import { reactive } from 'vue'

const counter = reactive({
  count: 0
})

console.log(counter.count) // 0
counter.count++

reactive()działa tylko na obiektach (w tym tablicach i typach wbudowanych, takich jak Mapi Set). 
ref(), z drugiej strony, może przyjąć dowolny typ wartości i utworzyć obiekt, który ujawnia wartość wewnętrzną w ramach właściwości .value:

const message = ref('Hello World!')

console.log(message.value) // "Hello World!"
message.value = 'Changed';


stan reaktywny zadeklarowany w bloku komponentu można wykorzystać bezpośrednio w szablonie. 
W ten sposób możemy renderować dynamiczny tekst na podstawie wartości obiektu counteri messageref, używając składni wąsów:

//<h1>{{ message }}</h1>
//<p>count is: {{ counter.count }}</p>

//np. 

<h1>{{ message }}</h1>
<p>count is: {{ counter.count }}</p>

Treść wewnątrz wąsów nie ogranicza się tylko do identyfikatorów lub ścieżek 
- możemy użyć dowolnego poprawnego wyrażenia JavaScript:

szablon
<h1>{{ message.split('').reverse().join('') }}</h1>

np.

<script setup>
import { reactive, ref } from 'vue'

const counter = reactive({ count: 0 })
const message = ref('Hello World!')
</script>

<template>
  <h1>{{ message }}</h1>
  <p>Count is: {{ counter.count }}</p>
</template>