# �^����� + TTS
## �ϥήM��
1. Vue.js 2.6.11
2. animate.css 4.1.0
3. bootstrap 4.5.0
4. speechSynthesis TTS

## Demo ���}
https://codepen.io/f416720001/full/wvMdmKQ

## TTS �ѦҺ��}�AVueJS��@��k�]�b����̤U��d��
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

## TTS �L�ج[�g�k
https://jsfiddle.net/f416720001/u2bm5a8f/1/

## �^�����Ѧ�youtube
https://www.youtube.com/watch?v=maFbo96YT8U

## Contact
To contact the authors:
Ying-Xiang Zhao, f416720001@gmail.com