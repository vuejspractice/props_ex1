<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input type="text" :value="msg" @input="changeMessage">
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: ""
    };
  },
  name: "HelloWorld",
  props: ["msg"],
  methods: {
    changeMessage(event) {
      this.message = event.target.value;
      this.$emit("messageChanged", this.message);
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
