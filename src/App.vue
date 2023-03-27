<template>
  <body>
  <div class="full-page">
    <header>
      <ul class="nav-list">
        <li class="nav-list-item">About</li>
        <li class="nav-list-item">Works</li>
        <li class="nav-list-item">Contact</li>
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
    <div class="about fade-in-on-scroll">
    <h2>About</h2>
      <p>1988年、神奈川県横浜市生まれ。<br>
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
  </div>
</body>
</template>

<style>

@import url('https://fonts.googleapis.com/css2?family=Inter&display=swap');

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


.title {
  margin: 40vh auto 0;
  text-align: center;
  letter-spacing: .2em;
  font-size: 2.25vw;
  font-family: 'Inter', sans-serif;
}

h2 {
  font-family: 'Inter', sans-serif;
}

.about {
  margin: 20%;
}

.fade-in-title {
  opacity: 1;
  animation-name: fadeIn;
  animation-duration: 2s;
  animation-delay: 0s;
  animation-fill-mode: forwards;
}

.fade-in-on-scroll {
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
      const el = this.$el.querySelector(".fade-in-on-scroll");
      if (!el) {
        return;
      }
      const elTop = el.getBoundingClientRect().top;
      const windowHeight = window.innerHeight;
      const yOffset = 100;
      if (elTop - windowHeight + yOffset <= 0) {
        el.classList.add("fade-in-on-scroll-active");
        window.removeEventListener("scroll", this.handleScroll);
      }
    }
  }
};
</script>