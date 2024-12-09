<template>
  <div class="main-wrapper">
    <div class="input-wrapper">
      <h1>Введите возраст!</h1>
      <input type="text" value="{{ inputValue }}" v-model="inputValue"/>
      <button @click="printValue(inputValue)" class="submitBtn">Подтвердить</button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      inputValue: ''
    };
  },
  name: "HomeView",
  components: {},
  methods: {
    printValue(inputValue) {
      alert('Поздравляю вам ' + inputValue + " лет!")
    }
  }
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
.main-wrapper {
  color: white;
  display: flex;
  justify-content: center;
  height: 100vh;
  background-color: #6d6d6d;
}
.input-wrapper{
  display: flex;
  flex-direction: column;
}
</style>