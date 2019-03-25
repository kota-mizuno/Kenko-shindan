<template>
  <div class="card answer">
    <p>あなたの診断結果は「{{result[score]}}」です。</p>
    <button class="button-is-info" @click="reload()">もう一度診断する</button>
    <hr>
    
    <p class ="share">結果をシェアしましょう!!</p>
    <a href="https://twitter.com/twitterjp?lang=ja" class="btn-social-circle btn-social-circle--twitter" target="_blank">
    <i class="fab fa-twitter"></i>
    </a>
    <a href="https://ja-jp.facebook.com/" class="btn-social-circle btn-social-circle--facebook" target="_blank">
    <i class="fab fa-facebook-f"></i>
    </a>
    <a href="https://akarie.co.jp/" class="btn-social-circle btn-social-circle--akarie" target="_blank">
    <i class="fas fa-home"></i>
    </a>
    <a href="https://line.me/ja/" class="btn-social-circle btn-social-circle--line" target="_blank">
    <i class="fab fa-line"></i>
    </a>
  </div>





</template>

<script>
export default {
  name: 'Answer',
  props: ['score'],
  data () {
    return {
      result: [
        '不健康',
        '普通',
        '健康'
      ]
    }
  },
  methods: {
    reload () {
      location.reload()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.share { 
  font-size: 0.4em;
  font-weight: 700;
  }

.answer {
  border-radius: 15px;
  padding: 3%;
  margin: 14%;
  height: 10vh;
  width: 70vw;
  background: #f8f8f8;
  font-size: 2.3em;
  font-weight:bold;
  color: #364e96;/*文字色*/
  border: solid 3px #364e96;/*線色*/
  padding: 0.4em;/*文字周りの余白*/
  border-radius: 0.5em;/*角丸*/
}




.button-is-info {
  display: inline-block;
  text-decoration: none;
  background: #fd9535;
  color: #FFF;
  width: 120px;
  height: 120px;
  line-height: 120px;
  border-radius: 50%;
  text-align: center;
  vertical-align: middle;
  overflow: hidden;
  box-shadow: 0px 0px 0px 5px #fd9535;
  border: dashed 1px #FFF;
  transition: .4s;
  margin: 3vh auto;
  font-weight: bold;
}

.button-is-info:hover {
  background: #5ab9ff;
  box-shadow: 0px 0px 0px 5px #5ab9ff;
}





.btn-social-circle {
  display: inline-block;
  position: relative;
  box-sizing: border-box;
  text-decoration: none;
  color: #FFF;
  width: 50px;
  height: 50px;
  line-height: 30px;
  padding: 5px;
  font-size: 25px;
  border-radius: 50%;
  text-align: center;
  vertical-align: middle;
  font-weight: bold;
  box-shadow: inset 0 2px 0px rgba(255, 255, 255, 0.25), inset 0 -2px 0px rgba(0, 0, 0, 0.18);
  transition: .2s;
}
.btn-social-circle .fa {
  line-height: 30px;
}
.btn-social-circle:hover {
  box-shadow: none;
}

.btn-social-circle--twitter {
  background: #1da1f3;
  border: solid 5px #1da1f3;
}

.btn-social-circle--facebook {
  background: #3b75d4;
  border: solid 5px #3b75d4;
}

.btn-social-circle--akarie {
  background: #ef4d4d;
  border: solid 5px #ef4d4d;
}

.btn-social-circle--line {
  background: #7ece46;
  border: solid 5px #7ece46;
  
}
</style>
