<template>
  <div>
    <span>about</span>
    <button @click="btnClick">点击</button>
  </div>
</template>

<script>
import emitter from './utils/eventBus'

export default {
  methods: {
    btnClick() {
      console.log("about click...")
      emitter.emit("foo", {name: "Jld", age: 30})
    },
  },
}
</script>

<style scoped></style>
