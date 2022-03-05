<template>
  <div class="input__box">
    <input
      type="text"
      placeholder="오늘의 할일을 작성해 보세요."
      v-model="newTodo"
      @keyup.enter="addTodo"
    />
    <button @click="addTodo">추가</button>
  </div>
</template>
<script>
export default {
  name: "TodoInput",
  data: () => ({
    newTodo: "",
  }),
  methods: {
    addTodo() {
      let value = this.newTodo && this.newTodo.trim();
      localStorage.setItem("todo", value);
      this.clearBox();
    },
    clearBox() {
      this.newTodo = "";
    },
  },
};
</script>
<style>
.input__box {
  display: flex;
  justify-content: center;
  margin-top: 100px;
}
.input__box input {
  border: 1px solid #eee;
  border-radius: 10px;
  padding: 10px 15px;
  outline: none;
  width: 600px;
  height: 50px;
  margin-right: 10px;
  box-shadow: 0 0px 3px rgb(0 0 0 / 5%);
  font-weight: 600;
}
.input__box button {
  border: none;
  outline: none;
  border-radius: 10px;
  padding: 10px 18px;
  box-shadow: 0 0px 3px rgb(0 0 0 / 5%);
  color: #222;
  background: #fff;
  cursor: pointer;
  font-weight: 600;
}
</style>
