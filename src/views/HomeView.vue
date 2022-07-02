<template>
  <main-navbar></main-navbar>
  <section>
    <div class="bg">
      <div class="container-fluid">
        <div class="title text-center text-light">
          <img src="../assets/minecraft.png" class="img-fluid" alt="minecraft" />
        </div>
      </div>
      <div class="container-fluid">
        <div class="server text-center d-flex justify-content-center align-self-center">
                    <input type="text" id="testing-code" :value="serversite">
                    <button class="copyserver" @click.stop.prevent="copyServer"><i class="bi bi-files"></i></button>
                    
                
        </div>
      </div>
    </div>
  </section>
  <latest-news></latest-news>
  <!-- introduction -->
  <div class="intro">
    <div class="container p-5">
      <div class="ninebox">
        <div class="product-wrap">
          <div class="product0 product1"></div>
        </div>
        <div class="product-wrap">
          <div class="product0 product2"></div>
        </div>
        <div class="product-wrap">
          <div class="product0 product3"></div>
        </div>
        <div class="product-wrap">
          <div class="product0 product4"></div>
        </div>
        <div class="product-wrap">
          <div class="product0 product5"></div>
        </div>
        <div class="product-wrap">
          <div class="product0 product6"></div>
        </div>
        <div class="product-wrap">
          <div class="product0 product7"></div>
        </div>
        <div class="product-wrap">
          <div class="product0 product8"></div>
        </div>
        <div class="product-wrap">
          <div class="product0 product9"></div>
        </div>
      </div>
    </div>
  </div>
  <!-- icons -->
  <div id="info" class="container p-5">
    <div class="row fw-bold">
      <div class="col-md-6 col-sm-12 row text-center mb-5">
        <div class="title mb-5 text-center fs-1 fw-bold">社群平台</div>
        <a class="col-6" href="https://www.facebook.com/codedriven/"
          ><img src="@/assets/homepage/fbicon.png" alt="粉專"
        /></a>
        <a class="col-6" href=""
          ><img src="@/assets/homepage/discord.png" alt="discord"
        /></a>
      </div>
      <div class="col-md-6 col-sm-12 row text-center mb-5">
        <div class="title mb-5 text-center fs-1 fw-bold">合作夥伴</div>
        <a class="col-6" href="https://www.sce.pccu.edu.tw/"
          ><img src="@/assets/homepage/ntcicon.png" alt="文大"
        /></a>
        <a class="col-6" href="https://www.codedriven.org/"
          ><img src="@/assets/homepage/codedrivenicon.png" alt="程式驅動"
        /></a>
      </div>
    </div>
  </div>
  <div id="server">
    <div class="container p-5 pt-0">
      <div class="d-flex flex-column justify-content-center">
        <div class="text-center mb-5 fs-1 fw-bold">伺服器狀態</div>
        <a href="https://minecraft-mp.com/server-s303741" target="_blank"
          ><img :src="leaderboard" class="w-100" alt="leaderboard"
        /></a>
      </div>
    </div>
  </div>

  <my-footer></my-footer>
</template>

<script>
import MainNavbar from "@/components/Home/MainNavbar.vue";
import LatestNews from "@/components/Home/LatestNews.vue";
import MyFooter from "../components/MyFooter.vue";
import Navbar from "../components/SubNavbar.vue";
import copy from 'copy-to-clipboard';


export default {
  name: "HomeView",
  data() {
    return {
      leaderboard: "https://minecraft-mp.com/leaderboard-303741-6.png",
      serversite: "mbc94.ntc.im",
    };
  },
  components: {
    MyFooter,
    MainNavbar,
    LatestNews,
    Navbar,
  },
  methods: {
    copyServer () {
          let testingCodeToCopy = document.querySelector('#testing-code')
          testingCodeToCopy.setAttribute('type', 'text')  
          testingCodeToCopy.select()

          try {
            var successful = document.execCommand('copy');
            alert('複製成功');
          } catch (err) {
            alert('複製失敗');
          }

        },

  }
};


</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
.intro {
  background-color: rgb(230, 227, 227);

}
section .bg {
  width: 100%;
  height: 100vh;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("@/assets/10950185.jpg");
  background-position: center;
  background-size: cover;
}
section .bg .title {
  letter-spacing: 30px;
  padding-top: 25vh;
}
section .bg .server {
  padding-top: 100px;
}
.server{
  background: url(@/assets/homepage/minecraftserversite.png) center no-repeat;
  height: 480px;
  padding-bottom: 50px;
}
.server input{
  color: #fff;
  background: transparent;
  outline:none;
  border:transparent solid 1px;
  align-self: center;
  height: 50px;
  font-size: 2em;

}
.copyserver
{   
    align-self: center;
    height: 50px;
    font-size: 2em;
    color: #fff;
    background: transparent;
    display: inline-block;
    text-decoration: none;
    letter-spacing: 2px;
    transition: 0.5s;
    border:transparent solid 1px;
}
  .ninebox {
    width: 450px;
    height: 450px;
    margin: 0 auto;
  }

.product-wrap {
  background: url(@/assets/bg/minecrafttu.png) rgba(255, 255, 255, 0.4);
  background-blend-mode: overlay;
  background-size: cover;
  position: relative;
  float: left;
  width: 150px;
  height: 150px;
  margin: 0px;
}
.product {
  background: white;
  position: absolute;
  top: 0;
  left: 0;
  width: 150px;
  height: 150px;
  transition: 0.2s;
}
.product0 {
  background: url(@/assets/homepage/black.png) center;
  background-size: contain;
  background-repeat: no-repeat;
  position: absolute;
  top: 0;
  left: 0;
  width: 150px;
  height: 150px;
  transition: 0.2s;
}
.product1 {
  background: url(@/assets/homepage/zombie.png) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product2 {
  background: url(@/assets/homepage/Chicken.png) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product3 {
  background: url(@/assets/homepage/Cow.png) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product3 p {
  text-align: center;
  display: flex; /* ★ */
  align-items: center;
}
.product4 {
  background: url(@/assets/homepage/zombie.png) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product6 {
  background: url(@/assets/homepage/castle.png) center;
  background-size: contain;
}
.product7 {
  background: url(@/assets/homepage/zombie.png) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product8 {
  background: url(@/assets/homepage/group.png) center;
  background-size: contain;
}
.product9 {
  background: url(@/assets/homepage/zombie.png) center;
  background-size: contain;
  background-repeat: no-repeat;
}

.product-wrap:hover .product1 {
  z-index: 100;
  width: 450px;
  height: 450px;
  top: 0px;
  background: url(@/assets/homepage/zombie.png) rgba(255, 255, 255, 0.8) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product-wrap:hover .product2 {
  z-index: 100;
  width: 450px;
  height: 450px;
  top: 0px;
  left: -150px;
  background: url(@/assets/homepage/Chicken.png) rgba(255, 255, 255, 0.8) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product-wrap:hover .product3 {
  z-index: 100;
  width: 450px;
  height: 450px;
  top: 0px;
  left: -300px;
  background: url(@/assets/homepage/Cow.png) rgba(255, 255, 255, 0.8) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product-wrap:hover .product4 {
  z-index: 100;
  width: 450px;
  height: 450px;
  top: -150px;
  background: url(@/assets/homepage/zombie.png) rgba(255, 255, 255, 0.8) center;
  background-size: contain;
  background-repeat: no-repeat;
}

.product-wrap:hover .product6 {
  z-index: 100;
  width: 450px;
  height: 450px;
  top: -150px;
  left: -300px;
  background: url(@/assets/homepage/castle.png) rgba(255, 255, 255, 0.8) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product-wrap:hover .product7 {
  z-index: 100;
  width: 450px;
  height: 450px;
  top: -300px;
  background: url(@/assets/homepage/zombie.png) rgba(255, 255, 255, 0.8) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product-wrap:hover .product8 {
  z-index: 100;
  width: 450px;
  height: 450px;
  top: -300px;
  left: -150px;
  background: url(@/assets/homepage/group.png) rgba(255, 255, 255, 0.8) center;
  background-size: contain;
  background-repeat: no-repeat;
}
.product-wrap:hover .product9 {
  z-index: 100;
  width: 450px;
  height: 450px;
  top: -300px;
  left: -300px;
  background: url(@/assets/homepage/zombie.png) rgba(255, 255, 255, 0.8) center;
  background-size: contain;
  background-repeat: no-repeat;
}

@media handheld, screen and (max-width: 786px) {
  .ninebox {
    width: 300px;
    height: 300px;
  }
  .product0 {
    width: 100px;
    height: 100px;
  }
  .product-wrap {
    width: 100px;
    height: 100px;
  }

  .product-wrap:hover .product1 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: 0px;
  }
  .product-wrap:hover .product2 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: 0px;
    left: -100px;
  }
  .product-wrap:hover .product3 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: 0px;
    left: -200px;
  }
  .product-wrap:hover .product4 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: -100px;
  }
  .product-wrap:hover .product5 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: -50px;
  }
  .product-wrap:hover .product6 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: -100px;
    left: -200px;
  }
  .product-wrap:hover .product7 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: -200px;
  }
  .product-wrap:hover .product8 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: -200px;
    left: -100px;
  }
  .product-wrap:hover .product9 {
    z-index: 100;
    width: 300px;
    height: 300px;
    top: -200px;
    left: -200px;
  }
}
</style>
