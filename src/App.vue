<template>
  <div id="app">
    <Quiz :question="test" :answers="answers" />
  </div>
</template>

<script>
import Quiz from './components/QuizChan.vue';

export default {
  name: 'App',
  components: {
    Quiz
  },
  data(){
    return{
      test: 'testaa'
      ,answers: [
        {id:1,contents:'回答1'}
        ,{id:2,contents:'回答2'}
        ,{id:3,contents:'回答3'}
        ,{id:4,contents:'回答4'}
    ]
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
