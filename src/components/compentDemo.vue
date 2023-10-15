<template>
  <div :class="{'red-bg': isComponent1, 'blue-bg': !isComponent1}">
    <div v-if="isComponent1">我是组件 1</div>
    <div v-else>我是组件 2</div>
    <button @click="onBackEvent">回传事件</button>
    <button @click="toggleComponent">切换组件</button>
  </div>
</template>

<script>
export default {
  name: "componentDemo",
  data() {
    return {
      isComponent1: true,
    };
  },
  methods: {
    onBackEvent() {
      alert('我是组件 1');
    },
    toggleComponent() {
      this.isComponent1 = !this.isComponent1;
    },
  },
};
</script>

<style>
.red-bg {
  background-color: red;
}

.blue-bg {
  background-color: blue;
}
</style>