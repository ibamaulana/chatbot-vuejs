<template>
  <div class="question-box">
    {{question}}
  </div>
</template>
<script>
export default {
  props:{
    question: {
      type:String,
      default: 'question'
    }
  },
}
</script>

<style scoped>
.question-box{
  align-self: flex-end;
  background: whitesmoke;
  border-radius: 12px;
  padding: 15px;
  font-size: 20px;
}
</style>