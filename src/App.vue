<template>
  <div id="app" class="container">
    <img width="25%" src="./assets/logo.png">
    <HelloWorld/>
    {{ text }}
    <input v-model="text"/>
    <Counter :startCount="6" @increased="show"/>
    <Counter :startCount="0"/>
    <Counter :startCount="12"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Counter from "./components/Counter";

export default {
  name: "App",
  data() {
    return {
      text: "Hi, how are you?",
      something: 5
    };
  },
  methods: {
    show(count) {
      alert(count);
    }
  },
  components: {
    HelloWorld,
    Counter
  }
};
</script>

<style>

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
