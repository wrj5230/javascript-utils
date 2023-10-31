<template>
    <div>
        {{question}}
        <button v-for="(answer,index) in answers" :key="index" v-on:click="clickAnswer(answer.id)">{{answer.contents}}</button>
    </div>
</template>

<script>
export default {
  name: 'QuizChan',
  methods:{
    clickAnswer: function(id){
      if(id==4){
        window.alert('正解！');
      }else{
        window.alert('残念！');
      }
    }
  },
  props: {
    question: String,
    answers: Array
  }
}
</script>