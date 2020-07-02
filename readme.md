![image_EnglishTest](https://github.com/f416720001/EnglishTestWithVueandTTS/blob/master/06252.png)
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
![image_RWD](https://github.com/f416720001/EnglishTestWithVueandTTS/blob/master/06253.png)

## 英文測驗參考youtube
https://www.youtube.com/watch?v=maFbo96YT8U

## 一些筆記
1. 叫停 setInterval()
函數內使用 clearInterval();
函數外使用 window.clearInterval(timeoutID);

2. 圓形倒數計時
實作：https://codepen.io/f416720001/pen/GRoOzoz
參考：https://www.youtube.com/watch?v=tNJCBw9FsPY

3. 做題完鎖住所有選項
html 增加一個class，叫做other;
vue 新增一個布林值 canAnswer，false時觸發other class;
other 使用 pointer-events: none 禁止所有滑鼠事件
<pre><code>
[css]
li.other {
  pointer-events: none;
}
[html]
<li
   v-for="option in options"
   @click.once="check(option)"
   :class="{ correct: status == '正確' && option.correct, error: status == '錯誤' && option.english == choosed.english, other: canAnswer == false}"
>
[javascript]
var vm = new Vue({
  data: {
    canAnswer: true
  },
  methods: {
    function() {
      this.canAnswer: false;
    }
  }
});
</code></pre>

4. 音效播放
<pre><code>
[javascript]
var file = new Audio("./audio/correct.mp3");
file.play();
</code></pre>

## Contact
To contact the authors:
Ying-Xiang Zhao, f416720001@gmail.com
