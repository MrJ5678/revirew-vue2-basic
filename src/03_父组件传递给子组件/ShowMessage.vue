<template>
  <div>
    <h1 :class="$attrs.class">{{ title }}</h1>
    <h2>{{ content }}</h2>
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  props: {
    title: {
      type: String,
      default: "空标题",
    },
    content: {
      type: String,
      default: "空内容",
      validator(value) {
        console.log(value)
        return true
      },
    },
  },
  mounted () {
    console.log(this.$attrs);
  }
}
</script>

<style scoped></style>
