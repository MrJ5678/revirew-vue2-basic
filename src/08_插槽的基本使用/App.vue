<template>
  <div>
    <my-slot-comp>
      <h2>组件中间</h2>
    </my-slot-comp>

    <my-slot-comp>
      <my-button />
    </my-slot-comp>

    <my-slot-comp />

    <my-slot-comp>
      <h2>第一段</h2>
      <h2>第二段</h2>
      <h2>第三段</h2>
    </my-slot-comp>
  </div>
</template>

<script>
import MySlotComp from "./MySlotComp.vue"
import MyButton from "./MyButton.vue"

export default {
  components: {
    MySlotComp,
    MyButton,
  },
}
</script>

<style scoped></style>
