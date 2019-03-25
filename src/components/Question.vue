<template>
  <section class="q-select">
    <h1>{{ question.message }}</h1>
    <hr>
    <button class="button is-info q-button"
         v-for="(s, idx) in question.select" :key="idx"
         @click="$emit('sum', s.score)">
      {{ s.text }}
    </button>
  </section>
</template>

<script>
export default {
  name: 'Question',
  props: ['question'],
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.q-select {
  margin: 15%;
  position: relative;/*相対位置*/
  padding-left: 1.2em;/*アイコン分のスペース*/
  line-height: 1.4;/*行高*/
  font-size: 2em;/*サイズ*/
}

.q-select:before {
  font-family: "Font Awesome 5 Free";
  content: "\f075";/*アイコンのユニコード*/
  position: relative;/*相対位置*/
  font-size: 2em;/*サイズ*/
  left: 0;/*アイコンの位置*/
  top: 20px;/*アイコンの位置*/
  color: #5ab9ff; /*アイコン色*/
}


.q-button {
  margin: 0.5em;
}
.q-button {
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

.q-button:active {
  /*押したとき*/
  box-shadow: 0 0 2px rgba(0, 0, 0, 0.30);
}
</style>
