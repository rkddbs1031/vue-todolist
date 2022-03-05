<template>
  <div class="home">
    <TodoHeader :msg="msg" />
    <TodoInput />
    <TodoList />
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
  }),
};
</script>
