<template>
  <div>
    <span>文章序号:</span>
    <input type="num" v-model="count" />
  </div>
</template>
<script>
export default {
  name: "login",
  data() {
    return {
      count: 1,
    };
  },
  watch: {
    count(val) {
      this.$store.dispatch("increment1", val);
    },
  },
  mounted() {
    this.$store.dispatch("increment1", 1);
  },
  methods: {},
};
</script>
<style scoped>
span {
  margin-left: 10px;
}
input {
  margin: 10px;
  height: 30px;
  width: 200px;
}
</style>
