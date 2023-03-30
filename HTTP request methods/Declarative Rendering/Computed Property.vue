Kontynuujmy budowanie na szczycie listy rzeczy do zrobienia z ostatniego kroku. 
Tutaj dodaliśmy już funkcję przełączania do każdego zadania. 
Odbywa się to poprzez dodanie donewłaściwości do każdego obiektu todo i użycie v-modeldo powiązania go z polem wyboru:

<li v-for="todo in todos">
    <input type="checkbox" v-model="todo.done">
    ...
  </li>
  