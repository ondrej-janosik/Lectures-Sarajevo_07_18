<template>
  <div class="container">
  {{ count }}
    <button @click="increase">Click me</button>
  </div>
</template>

<script>
export default {
  props: ["startCount"],
  data() {
    return {
      count: this.startCount
    };
  },
  methods: {
    increase() {
      this.count += 1;
      this.$emit('increased', this.count)
    }
  }
};
</script>

<style scoped>
.container {
  background-color: yellow;
}
</style>
