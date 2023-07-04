<template>
  <body>
  <div class="full-page">
    <header>
      <ul class="nav-list">
        <li class="nav-list-item"><a href="#about">About</a></li>
        <li class="nav-list-item"><a href="#works">Works</a></li>
        <li class="nav-list-item"><a href="#contact">Contact</a></li>
      </ul>
    </header>
    <br>
    <br>
    <br>
    <br>
    <h1 class="title fade-in-title">NORIFUMI OHASHI</h1>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <div class="about fade-in-on-scroll-about">
    <h2 id="about">About</h2>
      <p class="text">1988年、神奈川県横浜市生まれ。<br>
          桐蔭学園高等学校理数科卒。千葉大学工学部情報画像学科卒。<br>
          大学では、コンピュータサイエンスの基礎やプログラミングの実習などを学ぶ。<br>
          また、学生時代には家庭教師のアルバイトをし、高校生の数学を中心に教える。人に教えることの楽しさや、試験で結果を出してくれたことの嬉しさなどを体験する。<br>
          サークルはTRPG(テーブルトークRPG)やカタンやドミニオン等のボードゲームをする所に所属し、テーブルを囲んで人とコミュニケーションをとりながら物語を創っていく楽しさや、ボードゲームのルールとコンポーネント（UI・UXにつながる部分）の多様さに触れた。<br>
          <br>
          卒業後は脳梗塞で半身不随の父の介護をしながら、TechAcademy就職予備校 Javaコースでeラーニングをする。TechAcademyではJavaの基本から正規表現、データベースとの連携などを学ぶ。<br>
          母が他界し、父が介護施設に入ってからはmanaby関内駅前事業所に週5回通所し就労訓練（模擬就労）をした。Excel（VBA） Word PowerPoint Photoshop Illustratorなどをはじめ、HTML・CSS・JavaScriptのeラーニング動画を視聴して学習した。<br>
          さらにPHP＋Laravel、Vue.js3を書籍で独習し、Laravel・Vueを用いたWebアプリをそれぞれAWS EC2・github pagesにデプロイした。
      </p>
    </div>
    <div class="works fade-in-on-scroll-works">
      <h2 id="works">Works</h2>
      <h3>Illustrator</h3>
      <div class="categories">
      
        <div class="card">
          <img src="./assets/logo.png" alt="Illustrator logo">
          <p class="text">架空の企業のロゴ</p>
        </div>
        <div class="card">
          <img src="./assets/map.png" alt="Illustrator map">
          <p class="text">架空の地図</p>
        </div>
        <div class="card">
          <img src="./assets/apple.png" alt="Illustrator apple">
          <p class="text">架空のイベントのフライヤー</p>
        </div>
        <div class="card">
          <img src="./assets/okinawa.png" alt="Illustrator okinawa">
          <p class="text">架空の旅行会社のフライヤー</p>
        </div>
      </div>
      <h3>Web</h3>
      <div class="categories">
        <div class="card">
          <a href="https://asdf2501.github.io/attack-speed/" target="_blank">
          <img src="./assets/azurlane.png" alt="Web azurlane">
          <p class="text">ゲームの攻撃速度計算機<br>(Vue.js3,github pages)</p></a>
        </div>
        <div class="card">
          <a href="http://ec2-3-112-2-43.ap-northeast-1.compute.amazonaws.com/tweet" target="_blank">
          <img src="./assets/tweet.png" alt="Web tweet">
          <p class="text">つぶやきアプリ<br>(Laravel ,AWS EC2)</p></a>
        </div>
      
      </div>

    </div>
    <div class="contact fade-in-on-scroll-contact">
      <h2 id="contact">Contact</h2>
      <p class="text mail">asdf_2501[at]hotmail.com</p>
    </div>
    <br>
    <br>
    <br>
    <br>
    <br>
  </div>
</body>
</template>

<style>

@import url('https://fonts.googleapis.com/css2?family=Inter&display=swap');
@import url(http://fonts.googleapis.com/earlyaccess/notosansjp.css);

html {
    scroll-behavior: smooth;
}

body {
  margin: 0;
  padding: 0;
}

header {
  position: fixed;
  z-index: 999;
  top: 0;
  left: 0;
  width: 100%;
}

.full-page {
  background-color: #f5f5f5;
}

.nav-list {
  font-family: 'Inter', sans-serif;
  text-align: right;
  padding: 10px 0;
  margin: 0 auto;
}
.nav-list-item {
  list-style: none;
  display: inline-block;
  margin: 0 20px;
}

a,a:hover,a:visited{
    color: inherit;
    text-decoration: none;
}


.title {
  margin: 40vh auto 0;
  text-align: center;
  letter-spacing: .2em;
  font-size: 2.25vw;
  font-family: 'Inter', sans-serif;
}

.text {
  font-family: 'Noto Sans JP', sans-serif;
}

.mail {
  text-align: center;
}

h2 {
  font-family: 'Inter', sans-serif;
}
h3 {
  font-family: 'Inter', sans-serif;
}

.about {
  margin: 20%;
}
.works {
  margin: 20%;
}
.contact {
  margin: 20%;
}

.categories {
  display: flex;
  flex-wrap: wrap;
  justify-content: start;
}

.card {
  width: calc(33.33% - 10px);
  margin-bottom: 20px;
  padding: 10px;
  box-shadow: 2px 2px 6px rgba(0,0,0,.4);
  box-sizing: border-box;
  text-align: center;
}

.card img {
  max-width: 100%;
  height: auto;
  margin-bottom: 10px;
}

@media (max-width: 1023px) {
  .card {
    flex-basis: calc(50% - 10px);
  }
}

@media (max-width: 767px) {
  .card {
    flex-basis: calc(100% - 10px);
  }
}

.card text {
  align-items: flex-end
}


.fade-in-title {
  opacity: 1;
  animation-name: fadeIn;
  animation-duration: 2s;
  animation-delay: 0s;
  animation-fill-mode: forwards;
}

.fade-in-on-scroll-about {
  opacity: 0;
}

.fade-in-on-scroll-works {
  opacity: 0;
}

.fade-in-on-scroll-contact {
  opacity: 0;
}

.fade-in-on-scroll-active {
  opacity: 1;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-delay: 0s;
  animation-fill-mode: forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>

<script>
export default {
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
  handleScroll() {
    const elAbout = this.$el.querySelector(".fade-in-on-scroll-about");
    const elWorks = this.$el.querySelector(".fade-in-on-scroll-works");
    const elContact = this.$el.querySelector(".fade-in-on-scroll-contact");

    if (elAbout && elAbout.getBoundingClientRect().top - window.innerHeight + 100 <= 0) {
      elAbout.classList.add("fade-in-on-scroll-active");
    }

    if (elWorks && elWorks.getBoundingClientRect().top - window.innerHeight + 100 <= 0) {
      elWorks.classList.add("fade-in-on-scroll-active");
    }

    if (elContact && elContact.getBoundingClientRect().top - window.innerHeight + 100 <= 0) {
      elContact.classList.add("fade-in-on-scroll-active");
    }

    // if (elAbout && elWorks && elContact) {
    //   window.removeEventListener("scroll", this.handleScroll);
    // }
  }
}
};
</script>