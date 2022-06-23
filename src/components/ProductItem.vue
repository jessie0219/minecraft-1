<template>
  <div class="col-md-4">
    <button
      type="button"
      class="btn"
      data-bs-toggle="modal"
      data-bs-target="#staticBackdrop"
    >
      <div class="card">
        <div class="item-img">
          <img :src="images" class="card-img-top" alt="..." />
        </div>
        <div class="card-body">
          <p class="card-text fs-5">苦力帕T恤</p>
          <!-- <p class="card-text">
            <i class="bi bi-star-fill"></i>
            <i class="bi bi-star-fill"></i>
            <i class="bi bi-star-fill"></i>
            <i class="bi bi-star-fill"></i>
            <i class="bi bi-star-fill"></i>
          </p> -->
          <p class="card-text fs-5">$999</p>
          <!-- Button trigger modal -->
        </div>
      </div>
    </button>
  </div>
  <!-- Modal -->
  <div
    class="modal fade"
    id="staticBackdrop"
    data-bs-backdrop="static"
    data-bs-keyboard="false"
    tabindex="-1"
    aria-labelledby="staticBackdropLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="staticBackdropLabel">商品資訊</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body d-flex">
          <div class="container">
            <div class="text-center mt-2">
              <img src="@/assets/cloth.png" alt="" />
            </div>
            <div class="text-center">
              <p class="mt-2 text-center">商品名: 苦力帕T恤</p>
            </div>
            <div class="text-center">
              <p>價錢: $999</p>
            </div>
            <!-- <div class="text-center">
              <input type="number" name="" id="" />
            </div> -->
          </div>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-success" data-bs-dismiss="modal">
            去蝦皮看看
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductItem",
  data() {
    return {
      images: require("../assets/cloth.png"),
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
