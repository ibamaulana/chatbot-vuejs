<template>
  <div class="answer-box">
    {{answer}}
  </div>
</template>
<script>
export default {
  props:{
    answer: {
      type:String,
      default: 'answer'
    }
  },
}
</script>

<style scoped>
.answer-box{
  align-self: flex-start;
  padding: 10px;
  background: whitesmoke;
  border-radius: 12px;
  padding: 15px;
  font-size: 20px;
}
</style>