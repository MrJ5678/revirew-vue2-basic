<template>
  <div class="tabs-control">
    <template v-for="(title, index) in titles" :key="index">
      <span
        class="tabs-control-item"
        :class="{active: currentIndex === index}"
        @click="itemClick(index)"
      >
        {{ title }}
      </span>
    </template>
  </div>
</template>

<script>
export default {
  emits: ['changeIndex'],
  props: {
    titles: {
      type: Array,
      required: true,
      default() {
        return ["衣服", "鞋子", "裤子"]
      },
    },
  },
  data() {
    return {
      currentIndex: 0
    }
  },
  methods: {
    itemClick(index) {
      this.currentIndex = index
      this.$emit('changeIndex', index)
    }
  },
}
</script>

<style scoped>
.tabs-control {
  display: flex;
  justify-content: space-around;
}

.tabs-control-item.active {
  color: red;
}

span.tabs-control-item.active {
  border-bottom: 5px solid red;
  padding: 5px 10px;
}
</style>
