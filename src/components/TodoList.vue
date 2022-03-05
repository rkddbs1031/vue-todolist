<template>
  <div class="todo">
    <ul class="todo-list list">
      <li v-for="(item, idx) in lists" :key="idx">
        <span>{{ item }}</span>
        <div class="btn">
          <button type="button" class="removeBtn" @click="removeTodo">
            ❌
          </button>
          <button type="button" class="removeBtn" @click="removeTodo">
            ✍
          </button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "TodoList",
  data: () => ({
    lists: {},
  }),
  created() {
    this.test();
  },
  methods: {
    test() {
      console.log(this.lists);
    },
  },
};
</script>

<style scoped>
.todo {
  width: 100%;
  max-width: 1200px;
  margin: 50px auto 100px;
}
/* list */
.todo ul.list {
  width: 900px;
  margin: 0 auto;
  background: #fff;
  box-shadow: 0 0px 3px rgb(0 0 0 / 5%);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
}
.todo ul.list li {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid #eee;
  padding: 15px 25px;
  width: 100%;
}
.isCompleted {
  text-decoration: line-through;
}
.todo ul.list li label {
  margin-left: 20px;
  cursor: pointer;
}
.todo ul.list li button {
  border: none;
  background: #f8f7f7;
  border-radius: 10px;
  padding: 10px;
  cursor: pointer;
  margin-left: 10px;
}
</style>
