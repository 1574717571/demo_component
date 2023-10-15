<template>
  <div>
    <h1>我是组件 2</h1>
    <button @click="handleClick">回传事件</button>
  </div>
</template>

<script>
export default {
  methods: {
    handleClick() {
      this.$emit('event-back', '组件 2');
    },
  },
};
</script>

<style scoped>

</style>