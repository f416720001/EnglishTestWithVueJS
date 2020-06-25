![image](https://github.com/f416720001/EnglishTestWithVueandTTS/blob/master/06252.png)
# 英文測驗 + TTS
## 使用套件
1. Vue.js 2.6.11
2. animate.css 4.1.0
3. bootstrap 4.5.0
4. speechSynthesis TTS

## Demo 網址
https://codepen.io/f416720001/full/wvMdmKQ

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

## RWD 手機版排版
![image](https://github.com/f416720001/EnglishTestWithVueandTTS/blob/master/0625.png)

## 英文測驗參考youtube
https://www.youtube.com/watch?v=maFbo96YT8U

## Contact
To contact the authors:
Ying-Xiang Zhao, f416720001@gmail.com
