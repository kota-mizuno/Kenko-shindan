<template>
  <div class="base-container">
    <h1>タベスギケンシン</h1>
    <h2>Webでカンタン！ケンコウシンダン!</h2>
    <Question
      v-for="(q, idx) in question" :key="idx"
      :question="q"
      @sum="sum"
      v-if="idx===index">
    </Question>
    <Answer :score="total" v-if="(question.length - 1) < index"></Answer>
  </div>
</template>

<script>
import Question from '@/components/Question'
import Answer from '@/components/Answer'
export default {
  name: 'Base',
  components: {
    Question,
    Answer
  },
  methods: {
    sum (value) {
      this.total += value
      this.index++
    }
  },
  data () {
    return {
      index: 0,
      iscompleted: false,
      // json: require('@/assets/~json'),
      question: [
        {
          message: '間食はしますか？',
          select: [
            {
              text: 'はい',
              score: 0
            },
            {
              text: 'いいえ',
              score: 1
            }
          ]
        },
        {
          message: '昼食はどちらを食べたいですか？',
          select: [
            {
              text: 'こってり肉料理',
              score: 0
            },
            {
              text: 'さっぱり魚料理',
              score: 1
            }
          ]
        },
      ],
      total: 0
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: bold;
  font-family: 'Nico Moji';
  font-size: 30px;
  height:68px;
}

h2 {
  font-weight: normal;
  font-family: 'Nico Moji';
  height: 5px;
  font-size: 15px;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

h1:first-letter {
  font-size: 2em;
  color: #fa6429;
}
</style>
