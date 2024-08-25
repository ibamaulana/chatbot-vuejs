<template>
  <div class="input-container">
    <input class="text-input" v-model="inputText">
    <button class="button-input" @click="submit" :disabled="loading">
      <svg data-slot="icon" fill="currentColor" style="width:20px;height:20px" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <path d="M3.105 2.288a.75.75 0 0 0-.826.95l1.414 4.926A1.5 1.5 0 0 0 5.135 9.25h6.115a.75.75 0 0 1 0 1.5H5.135a1.5 1.5 0 0 0-1.442 1.086l-1.414 4.926a.75.75 0 0 0 .826.95 28.897 28.897 0 0 0 15.293-7.155.75.75 0 0 0 0-1.114A28.897 28.897 0 0 0 3.105 2.288Z"></path>
      </svg>
    </button>
  </div>
</template>
<script>
export default {
  data(){
    return{
      inputText:"",
      loading:false
    }
  },
  methods:{
    async submit(){
      this.loading = true
      const text = this.inputText
      this.inputText = ""
      await this.$emit('submitChat',text)
      this.loading = false
    }
  }
}
</script>


<style scoped>
.input-container{
  width: 50dvw;
  height: 150px;
  display: flex;
  gap: 10px;
  align-items: center;
}
.text-input{
  width: 100%;
  padding: 10px 20px;
  border: 1px solid gray;
  border-radius: 12px;
  height: 30px;
}
.button-input{
  width: 50px;
  height: 50px;
  padding: 5px 10px;
  border: 1px solid black;
  border-radius: 12px;
  background: whitesmoke;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>