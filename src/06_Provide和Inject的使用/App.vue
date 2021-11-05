<template>
  <div>
    <home />
  </div>
</template>

<script>
import Home from "./Home.vue"
export default {
  provide: {
    name: "Jld",
    age: 30,
  },
  components: {
    Home,
  },
}
</script>

<style scoped></style>
