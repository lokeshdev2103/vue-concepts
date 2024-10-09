<template>
  <div class="totalloyout">
    <div>
      <input v-model="newtodo" placeholder="enter a task" />
      <button @click="addTodo">Add Task</button>
    </div>
    <div>
      <p class="errormessage" v-if="errorMessage">{{ errorMessage }}</p>
    </div>
    <div>
      <table>
        <tr>
          <th>status</th>
          <th>task</th>
          <th>action</th>
        </tr>
        <tr  v-for="(todo, index) in todos" :key="index">
          <td>
            <input class="col2" type="checkbox" v-model="todo.completed" />
          </td>
          <td>
            <span class="col8" :class="{ completd: todo.completd }">{{todo.text}}</span>
          </td>
          <td>
            <button class="col4" @click="removetodo(index)">remove</button>
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>
<script>
import { ref } from "vue";

export default {
  setup() {
    const newtodo = ref("");
    const todos = ref([]);
    const errorMessage = ref("");

    const addTodo = () => {
      if (newtodo.value !== "") {
        errorMessage.value = "";
        todos.value.push({ text: newtodo.value, completed: true });
        newtodo.value = "";
      } else {
        errorMessage.value = " please enter the task";
      }
    };

    const removetodo = (index) => {
      todos.value.splice(index, 1);
    };

    return {
      newtodo,
      addTodo,
      todos,
      removetodo,
      errorMessage,
    };
  },
};
</script>
<style scoped>
.completed {
  text-decoration: line-through;
  color: aqua;
}
.errormessage {
  color: red;
}

table tr th,td{
  border: 2px solid red;
}
</style>