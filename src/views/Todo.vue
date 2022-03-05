<template>
  <div class="home">
    <TodoHeader />
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
};
</script>
