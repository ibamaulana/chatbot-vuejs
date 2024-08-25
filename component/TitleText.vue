<template>
  <p class="title" v-if="type == 'home'">Welcome to <br>My Personal Chatbot</p>
  <p class="subtitle" v-else>My Personal Chatbot</p>
</template>
<script>
export default {
  props:{
    type: {
      type:String,
      default: 'home'
    }
  },
  data(){
    return{
      homeText:"Welcome to My Personal Chatbot",
      chatText:"My Personal Chatbot"
    }
  }
}
</script>


<style scoped>
.title{
  font-size: 36px;
  text-align: center;
  height: 80px;
  display: flex;
  align-items: center;
}
.subtitle{
  font-size: 32px;
  text-align: left;
  height: 100px;
  height: 80px;
  display: flex;
  align-items: center;
}
</style>