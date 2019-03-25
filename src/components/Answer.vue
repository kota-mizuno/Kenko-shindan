<template>
  <div class="card answer">
    <p>あなたの診断結果は「{{result[score]}}」です。</p>
    <button class="button-is-info" @click="reload()">もう一度診断する</button>
    <hr>
    <a href="#" class="btn-social-icon-twitter">
      <span class="btn-social-icon-twitter__square"><i class="fab fa-twitter-square"></i></span> Share
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
.answer {
  border-radius: 15px;
  padding: 3%;
  margin: 15%;
  height: 20vh;
  width: 70vw;
  background: #f8f8f8;
  font-size: 2.2em;
  color: #364e96;/*文字色*/
  border: solid 3px #364e96;/*線色*/
  padding: 0.5em;/*文字周りの余白*/
  border-radius: 0.5em;/*角丸*/
}




.button-is-info {
  position: relative;
  display: inline-block;
  padding: 0.25em 0.5em;
  text-decoration: none;
  color: #FFF;
  background: #fd9535;/*色*/
  border-radius: 4px;/*角の丸み*/
  box-shadow: inset 0 2px 0 rgba(255,255,255,0.2), inset 0 -2px 0 rgba(0, 0, 0, 0.05);
  font-weight: bold;
  border: solid 2px #d27d00;/*線色*/
}

.button-is-info:active {
  /*押したとき*/
  box-shadow: 0 0 2px rgba(0, 0, 0, 0.30);
}

.btn-social-icon-twitter {
  text-decoration: none;
  display: inline-block;
  text-align: center;
  color: #1da1f3;
  font-size: 25px;
  text-decoration: none;
}

.btn-social-icon-twitter:hover {
  color:#88daff;
  transition: .5s;
}

.btn-social-icon-twitter__square {
  border-radius: 10px;
  position: relative;
  display: inline-block;
  width: 50px;
  height: 50px;
  font-size: 35px;
  line-height: 50px;
  vertical-align: middle;
  color: #FFF;
  background: #1da1f3;
}

.btn-social-icon-twitter__square i {
  line-height: 50px;
}
</style>
