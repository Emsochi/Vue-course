Oprócz otrzymywania rekwizytów komponent potomny może również emitować zdarzenia do rodzica:

<script setup>
// declare emitted events
const emit = defineEmits(['response'])

// emit with argument
emit('response', 'hello from child')
</script>

Pierwszym argumentem jest nazwa zdarzenia. Wszelkie dodatkowe argumenty są przekazywane do detektora zdarzeń.emit()

Rodzic może nasłuchiwać zdarzeń emitowanych przez dziecko za pomocą v-on- tutaj program obsługi otrzymuje dodatkowy argument z wywołania emisji dziecka i przypisuje go do stanu lokalnego:

<ChildComp @response="(msg) => childMsg = msg" />

    np.

<script setup>
import { ref } from 'vue'
import ChildComp from './ChildComp.vue'

const childMsg = ref('No child msg yet')
</script>

<template>
  <ChildComp />
  <p>{{ childMsg }}</p>
</template>

<script setup>
const emit = defineEmits(['response'])

emit('response', 'hello from child')
</script>

<template>
  <h2>Child component</h2>
</template>