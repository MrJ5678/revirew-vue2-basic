<template>
  <div>
    <show-message class="jld" v-bind="message"/>
    <mult-root-ele id="aaa"/>
  </div>
</template>

<script>
import ShowMessage from './ShowMessage.vue'
import MultRootEle from './MultRootEle.vue'

export default {
  components: {
    ShowMessage,
    MultRootEle
  },
  data() {
    return {
      message: {
        title: '标题',
        content: '内容'
      }
    }
  },
}
</script>

<style scoped></style>
