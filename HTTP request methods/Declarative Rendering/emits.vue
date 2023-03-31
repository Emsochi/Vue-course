Oprócz otrzymywania rekwizytów komponent potomny może również emitować zdarzenia do rodzica:

<script setup>
// declare emitted events
const emit = defineEmits(['response'])

// emit with argument
emit('response', 'hello from child')
</script>

Pierwszym argumentem jest nazwa zdarzenia. Wszelkie dodatkowe argumenty są przekazywane do detektora zdarzeń.emit()