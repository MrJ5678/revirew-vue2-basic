<template>
  <div>
    <navbar :name="name">
      <template #left>
        <button>左边部分</button>
      </template>
      <template v-slot:center>
        <h2>中间部分</h2>
      </template>
      <template v-slot:right>
        <i>右边部分</i>
      </template>
      <template v-slot:[name]>
        <i>右边部分</i>
      </template>
    </navbar>
  </div>
</template>

<script>
import Navbar from "./Navbar.vue"

export default {
  components: {
    Navbar,
  },
  data() {
    return {
      name: "jld"
    }
  },
}
</script>

<style scoped></style>
