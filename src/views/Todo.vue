<template>
  <div class="home">
    <TodoHeader :msg="msg" />
    <TodoInput @addTodo="addTodo" />
    <TodoList :lists="lists" @removeTodo="removeTodo" />
  </div>
</template>

<script>
import TodoHeader from "@/components/TodoHeader.vue";
import TodoInput from "@/components/TodoInput.vue";
import TodoList from "@/components/TodoList.vue";

export default {
  name: "Home",
  components: {
    TodoHeader,
    TodoInput,
    TodoList,
  },
  data: () => ({
    msg: "Todo List",
    lists: [],
  }),
  created() {
    if (localStorage.length > 0) {
      for (let i = 0; i < localStorage.length; i++) {
        this.lists.push(localStorage.getItem(localStorage.key(i)));
      }
    }
  },
  methods: {
    addTodo(item) {
      localStorage.setItem(item, item);
      this.lists.push(item);
    },
    removeTodo(item, idx) {
      localStorage.removeItem(item);
      this.lists.splice(idx, 1);
    },
  },
};
</script>
