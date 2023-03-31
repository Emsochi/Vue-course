Czasami może być konieczne reaktywne wykonanie „skutków ubocznych” - na przykład zalogowanie numeru do konsoli, gdy się zmieni. Możemy to osiągnąć dzięki obserwatorom:

import { ref, watch } from 'vue'

const count = ref(0)

watch(count, (newCount) => {
  // yes, console.log() is a side effect
  console.log(`new count is: ${newCount}`)
})