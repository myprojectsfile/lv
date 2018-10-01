<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button  class="btn btn-danger btn-sm"  @click="reset">reset</button>
    <button  class="btn btn-secondary btn-sm"  @click="myFunc()">run func</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
    myFunc: Function
  },
  methods: {
    reset() {
      this.msg = "سلام سلام همگی سلام";
      this.$emit("msgChanged", this.msg);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
