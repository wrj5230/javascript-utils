<template>
    <div>
      {{ currentQuestion.content }}
    </div>
  </template>
  
  <script>
  export default {
    name: 'QuestionBody',
    props: {
        qImageUrl: String,
    }
  }
  </script>
  