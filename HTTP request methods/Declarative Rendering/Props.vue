Komponent potomny może przyjmować dane wejściowe od rodzica za pośrednictwem właściwości . Najpierw musi zadeklarować rekwizyty, które akceptuje:

<!-- ChildComp.vue -->
<script setup>
const props = defineProps({
  msg: String
})
</script>

Note defineProps()to makro w czasie kompilacji i nie trzeba go importować. Po zadeklarowaniu msgrekwizytu można go użyć w szablonie komponentu potomnego. Dostęp do niego można również uzyskać w JavaScript za pośrednictwem zwróconego obiektu defineProps().

Rodzic może przekazać rekwizyt dziecku, tak jak atrybuty. Aby przekazać wartość dynamiczną, możemy również użyć v-bindskładni:

<ChildComp :msg="greeting" />