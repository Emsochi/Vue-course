Możemy poprosić o ref szablonu - czyli odniesienie do elementu w szablonie - używając specjalnego refatrybutu :

<p ref="p">hello</p>

Aby uzyskać dostęp do ref, musimy zadeklarować ref o pasującej nazwie:

const p = ref(null)

Zauważ, że ref jest inicjowany nullwartością. Dzieje się tak, ponieważ element jeszcze nie istnieje, gdy jest wykonywany. Szablon ref jest dostępny tylko po zamontowaniu komponentu .<script setup>

//Aby uruchomić kod po zamontowaniu, możemy użyć onMounted()funkcji:

import { onMounted } from 'vue'

onMounted(() => {
  // component is now mounted.
})

//<script setup>
//import { ref, onMounted } from 'vue'

const p = ref(null)

onMounted(() => {
  p.value.textContent = 'mounted!'
})
</script>

<template>
  <p ref="p">hello</p>
</template>