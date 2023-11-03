<template>
  <div>
    <QuestionHead :qTitle="currentQuestion.content" />
    <QuestionBody v-if="currentQuestion.imageUrl!=null" :qImageUrl="currentQuestion.imageUrl" />
  </div>
</template>

<script>
import QuestionHead from "./Question/QuestionHead.vue";
import QuestionBody from "./Question/QuestionBody.vue";

export default {
  name: "MainQuestion",
  components: {
    QuestionHead: QuestionHead,
    QuestionBody: QuestionBody,
  },
  props: {
    questions: Array,
  },
  data() {
    return {
      currentQuestion: {},
    };
  },
  created() {
    this.chooseQuestion();
  },
  methods: {
    chooseQuestion() {
      const index = Math.floor(Math.random() * this.questions.length);
      this.currentQuestion[index];
    },
  },
};
</script>
