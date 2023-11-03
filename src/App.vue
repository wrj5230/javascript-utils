<template>
  <div id="app">
    <Quiz :question="questions" />
    <Answer :question="answers" :answers="answers" />
  </div>
</template>

<script>
import Question from "./components/Question.vue";
import Answer from "./components/Answer.vue";

export default {
  name: "App",
  components: {
    Quiz: Question,
    Answer: Answer,
  },
  data() {
    return {
      questions: [
        { id: 1, name: "問一", imageUrl: "", content: "この画像は誰でしょう" },
      ],
      answers: [
        [
          { id: 1, content: "回答1", hit: true },
          { id: 2, content: "回答2", hit: false },
          { id: 3, content: "回答3", hit: false },
          { id: 4, content: "回答4", hit: false },
        ],
      ],
    };
  },
};
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
