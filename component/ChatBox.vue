<template>
  <div class="chatbox-container">
    <slot name="chat"/>
  </div>
</template>
<script>
export default {
}
</script>

<style scoped>
.chatbox-container{
  overflow: auto;
  height: calc(100dvh - 80px - 150px);
  width: 50dvw;
  display: flex;
  flex-direction: column;
}
</style>