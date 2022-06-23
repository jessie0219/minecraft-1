<template>
  <div class="about">
    <div class="background">
      <img :src="background" alt="" />
      <MainNavbar></MainNavbar>
    </div>
    <div class="info text-start shadow-lg">
      <div class="content p-4">
        <i class="fa-solid fa-circle-info my-4"><p>　什麼是 Minecraft</p></i>

        <p class=" ">
          微軟旗下Mojang Studios開發的沙盒遊戲。
          玩家可以在一個3D世界內與方塊進行互動。
          遊戲中的特色功能包括探索世界、採集資源、合成物品及生存冒險等。
          有著多種模式的Minecraft，在台灣是個家喻戶曉的遊戲，也有教育機構會以「玩賣塊學程式」來教導小朋友邏輯思考。
          Minecraft是個能邊玩邊學的遊戲，還沒玩過的朋友們快一起加入賣塊行列吧 !
        </p>
        <hr />
        <br />
        <i class="fa-solid fa-circle-info">
          <p>　為何要舉辦麥塊建築大賽？</p>
        </i>

        <p class=" ">
          <br />
          當身為家長的我們，
          看到從2020年起許多大學、高中、國中開始有不同麥塊愛好者，
          因疫情設計虛擬校園及虛擬畢業典禮，
          我們認為可以引導小朋友在創意創造及程式學習上使用Minecraft，
          並因應108新課綱高中以下可能需要學習歷程(研習/獎勵證書)在未來升學使用，
          故與國立臺北護理健康大學合作並邀請全台大專院校共襄盛舉，
          讓小朋友在開心的創作中參與競賽，獲得學習歷程證明也充足自己團隊協做的信心，
          因此舉辦麥塊建築大賽。
        </p>
        <hr />
        <br />

        <i class="fa-solid fa-circle-info">
          <p>　Minecraft 是一個這樣的遊戲</p>
        </i>
        <br />
        <p class=" ">
          <br />
          Majong 研究中心主管賽克斯·佩爾森（Saxs Persson）表示:
          「讓人們可以建造屬於自己的 Minecraft，這很重要，
          這款遊戲最強調的就是個人體驗。
          這樣能鼓勵更多的人們去建造自己想要建造的東西。」
        </p>
        <br />
      </div>
    </div>
    <my-footer></my-footer>
  </div>
</template>

<script>
import MainNavbar from "@/components/Home/MainNavbar.vue";
import SubNavbar from "../components/SubNavbar.vue";
import MyFooter from "../components/MyFooter.vue";

export default {
  name: "AboutView",
  components: {
    MainNavbar,
    SubNavbar,
    MyFooter,
  },
  data() {
    return {
      background: require("../assets/about/about-background.png"),
    };
  },
};
</script>

<style scoped>
.background {
  max-width: 3000px;
  max-height: 40vh;
  overflow: hidden;
  /* z-index: 1; */
  /* background-image: url(./assets/5.jpg);
background-repeat: no-repeat;
background-attachment: fixed;
background-position: center;
background-size: cover;
max-width: 100%;
height:30vh */
}
.background img {
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: fixed;
  object-position: right bottom;
  z-index: 1;
}
.info {
  width: 80%;
  height: 100%;
  margin: 0 auto;
  margin-top: -70px;
  margin-bottom: 50px;
  white-space: normal;
  /* z-index:-100; */
  position: relative;
  background: white;
}

p {
  font-family: "Josefin Sans", sans-serif;
  display: inline-block;
}

@media screen and (max-width: 768px) {
  .info {
    width: 100%;
    margin-top: 0;
    margin-bottom: 0;
    padding-top: 20px;
  }
  .content {
    font-size: 15px;
    /* flex-grow: 1; */
  }
}
</style>
