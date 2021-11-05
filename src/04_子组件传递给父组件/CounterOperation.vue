<template>
  <div>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>

    <input type="text" v-model.number="num">
    <button @click="incrementN">+n</button>
  </div>
</template>

<script>
  export default {
    // emits: ['add', 'sub', 'addN'],
    emits: {
      add: null,
      sub: null,
      addN: payload => {
        console.log(payload)
        return true
      }
    },
    data() {
      return {
        num: 1
      }
    },
    methods: {
      increment() {
        // console.log('+1')
        this.$emit("add")
      },
      decrement() {
        // console.log('-1')
        this.$emit("sub")
      },
      incrementN() {
        // console.log(`+${this.num}`)
        this.$emit('addN', this.num)
      }
    },
  }
</script>

<style scoped>

</style>