<template>
  <div>
    <span>HomeContent</span>
  </div>
</template>

<script>
import emitter from './utils/eventBus'

export default {
  created () {
    emitter.on('foo', (info) => {console.log(info)});
  },
}
</script>

<style scoped></style>
