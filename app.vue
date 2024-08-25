<template>
  <div class="main-container">
    <title-text
      :type="chatHistory.length?'chat':'home'"
    />
    <chat-box v-if="chatHistory.length">
      <template #chat>
        <template v-for="chat in chatHistory" :key="`chat${chat.id}`">
          <question-box 
            :question="chat.question"
          />
          <answer-box
            :answer="chat.answer"
          />
        </template>
      </template>
    </chat-box>
    <input-container
      @submit-chat="submitChat"
    />
  </div>
</template>
<script>
import AnswerBox from './component/AnswerBox.vue'
import ChatBox from './component/ChatBox.vue'
import InputContainer from './component/InputContainer.vue'
import QuestionBox from './component/QuestionBox.vue'
import TitleText from './component/TitleText.vue'
export default {
  components: { TitleText, InputContainer, ChatBox, QuestionBox, AnswerBox },
  data(){
    return {
      chatHistory:[]
    }
  },
  methods:{
    async submitChat(text){
      console.log('submit')
      this.chatHistory.push({
        question:text,
        answer:'Heloo this is template answer'
      })
    }
  }
}
</script>
<style>
body{
  margin: 0!important;
}
.main-container{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100dvh;
}
</style>
