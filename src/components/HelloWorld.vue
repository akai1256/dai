<template>
  <div class="hello">
    <h1>小文字→大文字</h1>
    <input v-model="lowerCase"/>→
    <input :value="upperCase" readonly/>

  </div>
</template>

<script>
export default {
  //要素を定義しないと要素をいじれないから定義した方が良いよ
  data() {
    return {
      //stringにnullはやめよう
      //nullは文字ではないから
      lowerCase: '',
    }
  },
  //要素いじりたいときに使うといいよ。ベタ書きすると可読性が落ちちゃうからね
  computed: {
    //今回のページの命のファンクションだよ
    //要素lowerCaseを大文字に変換してくれいるよ。
    upperCase() {
      return this.lowerCase.toUpperCase();
    }
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
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
</style>
