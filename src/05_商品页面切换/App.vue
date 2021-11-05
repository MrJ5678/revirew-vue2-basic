<template>
  <div>
    <tab-control :titles="titles" @changeIndex="changeView"/>
  </div>
</template>

<script>
import TabControl from "./TabControl.vue"
export default {
  components: {
    TabControl,
  },
  data() {
    return {
      titles: ["衣服", "鞋子", "裤子"],
    }
  },
  methods: {
    changeView(index) {
      console.log(index)
    }
  },
}
</script>

<style scoped></style>
