Komponent potomny może przyjmować dane wejściowe od rodzica za pośrednictwem właściwości . Najpierw musi zadeklarować rekwizyty, które akceptuje:

<!-- ChildComp.vue -->
<script setup>
const props = defineProps({
  msg: String
})
</script>