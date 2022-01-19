divd
<template>
  <div>
    <div class="news">
      <div class="news-wrapper">
        <span>【2022.10.01更新】</span><br />
        <span>期間限定イベント</span>
        <span class="text-weight"
          >「見習い魔女のキラキラ★TWILIGHT NIGHT HALLOWEEN」</span
        >
        <span>開催！</span>
      </div>
    </div>
    <img class="top-img" id="top-img1" src="../assets/min_Original.png" />
    <div class="prologue">
      <div id="prologue-title" class="fade">－PROLOGUE－</div>
      <div class="prologue-text-wrapper fade" id="prologue-text-wrapper-1">
        <div class="prologue-text" id="text1">
          <span
            >10月31日はグリッタタウンで一番大切な日。<br />日々の平穏を願い、<br />町中はカボチャの妖精の光に包まれる。</span
          >
        </div>
      </div>
      <div class="prologue-text-wrapper fade" id="prologue-text-wrapper-2">
        <div class="prologue-text" id="text2">
          <span
            >町の人々に妖精を届けるために、<br />魔女は年中大忙し。<br />「キラキラの魔女」で、カボチャは<br />人々の願いに姿を変える。</span
          >
        </div>
      </div>
      <div class="prologue-text-wrapper fade" id="prologue-text-wrapper-3">
        <div class="prologue-text" id="text3">
          <span
            >____今年も大切なあの日が近づいてきた。<br />魔女は今日も大忙し。</span
          >
        </div>
        <div class="prologue-text" id="text4">
          <span
            >見習い魔女のガーベラは、<br />今日も魔法の練習。<br />「キラキラの魔女」はまだ使えない。</span
          >
        </div>
      </div>
      <div class="prologue-text-wrapper fade" id="prologue-text-wrapper-4">
        <div class="prologue-text" id="text5">
          <span
            >大切な日を目前としたある日、<br />魔女は突然姿を消す。<br />しかし、<br />町のシンボルとなる「カボチャの大妖精」<br />がまだ完成していない。</span
          >
        </div>
      </div>
      <div class="prologue-text-wrapper fade" id="prologue-text-wrapper-5">
        <div class="prologue-text" id="text6">
          <span
            >突然魔女の代役を任されたガーベラは、<br />魔女としての役目を果たすことが出来るのか____</span
          >
        </div>
      </div>
    </div>
    <div class="gerbera-wrapper">
      <div class="stars fade">
        <img src="../assets/star1.png" class="star" v-for="i in 5" :key="i" />
      </div>
      <img src="../assets/gerbera-name.png" class="gerbera-name fade" />
      <img src="../assets/gerbera.png" class="gerbera fade" />
      <img src="../assets/gerbera-mini.png" class="gerbera-mini fade" />
    </div>
    <div class="gerbera-prologue-wrapper">
      <div class="gerbera-prologue fade">
        <span
          >代々町の風習を守る魔女一家の見習い魔女。<br />母が突然失踪し、急に魔女の仕事を引き継ぐことになった。<br />しかし、いつもカボチャの妖精以外を生み出してしまう。<br />いつも一緒にいるカボチャの妖精は、幼いひに母からもらった「ぱぷ子」。カボチャの妖精はハロウィンの日に消えてしまうが、ぱぷ子はなぜか消えない。</span
        >
      </div>
    </div>
    <div class="brad-wrapper">
      <div class="stars fade">
        <img src="../assets/star1.png" class="star" v-for="i in 5" :key="i" />
      </div>
      <img src="../assets/brad-name.png" class="brad-name fade" />
      <img src="../assets/brad.png" class="brad fade" />
      <img src="../assets/brad-mini.png" class="brad-mini fade" />
    </div>
    <div class="brad-prologue-wrapper">
      <div class="brad-prologue fade">
        <span
          >代々町の風習を守る魔女一家の見習い魔女。<br />母が突然失踪し、急に魔女の仕事を引き継ぐことになった。<br />しかし、いつもカボチャの妖精以外を生み出してしまう。<br />いつも一緒にいるカボチャの妖精は、幼いひに母からもらった「ぱぷ子」。カボチャの妖精はハロウィンの日に消えてしまうが、ぱぷ子はなぜか消えない。</span
        >
      </div>
    </div>
  </div>
</template>

<script>
import $ from 'jquery'

export default {
  mounted: function () {
    $(window).scroll(function () {
      $('.prologue .fade').each(function () {
        var imgPos = $(this).offset().top
        var scroll = $(window).scrollTop()
        var windowHeight = $(window).height()
        if (scroll > imgPos - windowHeight + windowHeight / 5) {
          $(this).addClass('on')
        } else {
          $(this).removeClass('on')
        }
      })
      $(
        '.gerbera-wrapper .fade, .gerbera-prologue-wrapper .fade, .brad-wrapper .fade, .brad-prologue-wrapper .fade'
      ).each(function () {
        var imgPos = $(this).offset().top
        var scroll = $(window).scrollTop()
        var windowHeight = $(window).height()
        if (scroll > imgPos - windowHeight + windowHeight / 5) {
          $(this).addClass('on1')
        } else {
          $(this).removeClass('on1')
        }
      })
    })
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Hachi+Maru+Pop&family=Zen+Maru+Gothic:wght@500&display=swap%27');
.prologue {
  font-family: 'Hachi Maru Pop' !important;
}
/* animation style */
.fade {
  opacity: 0;
  -webkit-transition: all 1s;
  -moz-transition: all 1s;
  -o-transition: all 1s;
  -ms-transition: all 1s;
  transition: all 1s;
}
.fade.on,
.fade.on1 {
  opacity: 1;
}
.fade.on:nth-of-type(1) {
  transition-delay: 0s;
}
.fade.on:nth-of-type(2) {
  transition-delay: 0.1s;
}
.fade.on:nth-of-type(3) {
  transition-delay: 0.2s;
}
.fade.on:nth-of-type(4) {
  transition-delay: 0.3s;
}
.fade.on:nth-of-type(5) {
  transition-delay: 0.4s;
}
.fade.on:nth-of-type(6) {
  transition-delay: 0.5s;
}
.fade.on1:nth-of-type(1) {
  transition-delay: -0.5s;
}
.fade.on1:nth-of-type(2) {
  transition-delay: 0s;
}
/* animation style */
.news {
  width: 100%;
  height: fit-content;
  background-color: rgb(255, 250, 232);
  padding: 20px 0;
  display: flex;
  align-items: center;
  justify-content: center;
}
.news-wrapper {
  width: 95%;
}
.news .text-weight {
  font-weight: 600;
}
.top-img {
  width: 100%;
  height: auto;
}
.prologue {
  background-image: linear-gradient(
    to bottom,
    #ffffff00 0%,
    #ffffffd3 30%,
    #f1f1f196 50%,
    #e6e6e696 70%,
    #ffffffba 90%,
    #ffffffbd 100%
  );
  padding: 0 30px;
}
#prologue-title {
  font-size: 9vw;
  width: fit-content;
  margin: 40px auto;
  -webkit-text-stroke: 1.5px rgb(255, 255, 255);
}
.prologue-text-wrapper {
  margin: 50px 0 50px 0;
}
#prologue-text-wrapper-2 {
  display: flex;
  justify-content: flex-end;
}
#prologue-text-wrapper-3 {
  display: flex;
  align-items: center;
  flex-direction: column;
  width: fit-content;
}
#prologue-text-wrapper-3 #text3 {
  margin-bottom: 20px;
}
#prologue-text-wrapper-4 {
  display: flex;
  justify-content: flex-end;
  padding-right: min(3vw, 80px);
}
#prologue-text-wrapper-5 {
  display: flex;
  justify-content: center;
  margin-bottom: 0;
}
.prologue-text {
  text-align: center;
  width: fit-content;
  font-size: 3.5vw;
  line-height: 120%;
}
.gerbera-wrapper {
  width: 100%;
  background-image: linear-gradient(
    to bottom,
    #ffffffa8 0%,
    #ffffff 40%,
    #ffffff 60%,
    #ffffffbd 100%
  );
  padding-top: 100px;
  height: 130vw;
  position: relative;
  overflow: hidden;
}
.stars {
  left: min(9vw, 100px);
  position: absolute;
}
.star {
  width: 5vw;
}
.gerbera-name {
  position: absolute;
  width: 50vw;
  top: min(31vw, 140px);
  left: 20px;
  z-index: 10;
}
.gerbera {
  position: absolute;
  width: 90%;
  top: min(30vw, 150px);
  right: -40px;
}
.gerbera-mini {
  position: absolute;
  width: 45%;
  left: 10px;
  bottom: 0;
}
.gerbera-prologue-wrapper {
  width: 100%;
  background-image: linear-gradient(to bottom, #ffffffa8 0%, #ffffff83 100%);
  padding-bottom: 10vw;
}
.gerbera-prologue {
  font-size: 2.5vw;
  width: 80%;
  margin: 0 auto;
  word-break: break-all;
}
.brad-wrapper {
  width: 100%;
  background-image: linear-gradient(
    to bottom,
    #ffffffa8 0%,
    #ffffff 40%,
    #ffffff 60%,
    #ffffffbd 100%
  );
  padding-top: 100px;
  height: 111vw;
  position: relative;
  z-index: 10;
  overflow: hidden;
}
.brad-name {
  position: absolute;
  width: 35vw;
  top: min(31vw, 170px);
  left: min(7vw, 60px);
}
.brad {
  position: absolute;
  width: 107%;
  top: min(44vw, 350px);
  right: -50px;
}
.brad-mini {
  position: absolute;
  width: 45%;
  left: 10px;
  bottom: 0;
}
.brad-prologue-wrapper {
  width: 100%;
  background-image: linear-gradient(to bottom, #ffffffa8 0%, #ffffff83 100%);
  padding-bottom: 20vw;
  z-index: 1;
}
.brad-prologue {
  font-size: 2.5vw;
  width: 80%;
  margin: 0 auto;
  word-break: break-all;
}
</style>
