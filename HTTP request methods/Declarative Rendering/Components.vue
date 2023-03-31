Do tej pory pracowaliśmy tylko z jednym komponentem. Aplikacje Real Vue są zwykle tworzone za pomocą zagnieżdżonych komponentów.

Komponent nadrzędny może renderować inny komponent w swoim szablonie jako komponent podrzędny. Aby użyć komponentu potomnego, musimy go najpierw zaimportować:

import ChildComp from './ChildComp.vue'

Następnie możemy użyć komponentu w szablonie jako:

<ChildComp />

<script setup>
import ChildComp from './ChildComp.vue'
</script>

<template>
  <ChildComp />
</template>