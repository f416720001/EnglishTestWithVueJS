# 英文測驗 + TTS
## 使用套件
1. Vue.js 2.6.11
2. animate.css 4.1.0
3. bootstrap 4.5.0
4. speechSynthesis TTS

## TTS 參考網址，VueJS實作方法也在此串最下方留言
https://gist.github.com/Eotones/d67be7262856a79a77abeeccef455ebf#gistcomment-3353454

<pre><code>
var vm = new Vue({
  el: "#app",
  data: {
    synth: window.speechSynthesis
  },
  methods {
    speak(msg) {
      console.log(msg);
      let u = new SpeechSynthesisUtterance();
      u.text = msg;
      this.synth.speak(u);
    }
  }
}
</code></pre>

## TTS 無框架寫法
https://jsfiddle.net/f416720001/u2bm5a8f/1/

## Demo 網址
https://codepen.io/f416720001/full/wvMdmKQ


# 趙映翔 2020/06/25