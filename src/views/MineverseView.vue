<template>
  <section>
    <MainNavbar></MainNavbar>
  </section>
  <section class="container-fluid main-background"></section>
  <section class="container-fluid container main-products">
    <div class="main">
      <div class="container-md products">
        <div class="row">
          <div class="col mb-3">
            <h1 class="mt-5 text-center fs-1 fw-bolder">元宇宙商圈</h1>
          </div>
        </div>
        <div class="row card-items g-5 p-5">
          <MineverseProductItem></MineverseProductItem>
        </div>
      </div>
    </div>
  </section>
  <MyFooter></MyFooter>
</template>

<script>
import MainNavbar from "@/components/Home/MainNavbar.vue";
import SubNavbar from "../components/SubNavbar.vue";
import MineverseProductItem from "../components/MineverseProductItem.vue";
import MyFooter from "../components/MyFooter.vue";

export default {
  name: "ProductsView",
  components: {
    MainNavbar,
    SubNavbar,
    MineverseProductItem,
    MyFooter,
  },
};
</script>

<style scoped>
/* main-background */
.main-background {
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url(@/assets/bg/2022-04-22_02.49.37.png);
  background-repeat: no-repeat;
  background-position: center;
  height: 70vh;
}
/* 產品項目區塊 */
.main {
  position: relative;
  box-shadow: 6px 6px 10px rgba(128, 128, 128, 0.5);
  background-color: #fff;
  top: -50vh;
  border-radius: 10px;
}
.main-products {
  padding: 0;
}
@media screen and (max-width: 1400px) {
  .main {
    border-radius: 0;
  }
}
@media screen and (max-width: 786px) {
  /* .main-background{
            height: 50vh;
            background-size: cover;
        } */
  .main {
    box-shadow: none;
    border-radius: 0;
  }
}
/* 卡片內容 */
.card {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}
.card:hover {
  cursor: pointer;
  transform: scale(1.1);
  transition: transform 0.5s ease;
}
/* .item-img{
        width: 100%;
    } */
.card-img-top {
  width: 100%;
  height: 20rem;
  object-fit: scale-down;
}

.bi-star-fill {
  color: rgb(255, 208, 0);
}
</style>
