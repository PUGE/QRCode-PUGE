<template>
  <div id="app">
    <vue-qr :text="text" :autoColor='true' :logoSrc="src2" :size="400" :margin="0"></vue-qr>
    <vue-qr text="Hello world!" :autoColor='true' :bgSrc="src" :logoSrc="src2" :size="400" :margin="0" style="margin-top:30px" :dotScale="0.35">
    </vue-qr>
    <vue-qr :text="testNumber"></vue-qr>
  </div>
</template>

<script>
import VueQr from '../../src/main'
export default {
  name: 'app',
  components: {
    VueQr
  },
  data() {
    return {
      src: require('./assets/bg1.png'),
      src2: require('./assets/avatar.png'),
      text: 'testtttt',
      testNumber: '0'
    }
  },
  mounted() {
    setInterval(() => {
      const num = Number(this.testNumber) + 1
      this.testNumber = String(num)
    }, 500)
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
