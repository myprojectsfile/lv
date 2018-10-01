<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld :msg="message" @msgChanged="message=$event" :myFunc="logto"/>
    <button class="btn btn-primary btn-sm" @click="changeMsg">change message</button>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  data: () => {
    return {
      message: "سلام به دوستان گلم"
    };
  },
  methods: {
    changeMsg() {
      this.message = "سلام به همه شما عزیزان";
    },
    logto() {
      alert('this is me');
    }
  },
  components: {
    HelloWorld
  }
};
</script>

<style>

#app {
  font-family: "calibri", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
