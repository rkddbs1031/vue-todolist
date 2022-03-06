<template>
  <div id="header">
    <h2>{{ msg }}</h2>
  </div>
</template>

<script>
export default {
  name: "TodoHeader",
  data: () => ({}),
  props: {
    msg: String,
  },
  created() {
    this.test();
  },
  methods: {
    test() {
      // console.log();
    },
  },
};
</script>
<style scoped>
#header h2 {
  text-align: center;
  border-bottom: 1px solid #eee;
  font-size: 30px;
  padding: 25px 0;
  color: #42b983;
  background: #fff;
}
</style>
