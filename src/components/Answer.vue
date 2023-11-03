<template>
    <div>
        <button v-for="(answer,index) in answers" :key="index" v-on:click="clickAnswer(answer.hit)">{{answer.content}}</button>
    </div>
</template>

<script>
export default {
  name: 'MainAnswer',
  methods:{
    clickAnswer: function(hit){
      if(hit){
        window.alert('正解！');
      }else{
        window.alert('残念！');
      }
    }
  },
  props: {
    answers: Array
  }
}
</script>