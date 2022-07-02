<template>
  <section>
    <nav class="navbar navbar-expand-lg fixed-top" id="nav">
      <div class="container">
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-icon text-light"
            ><i class="fa-solid fa-bars"></i
          ></span>
        </button>
        <!-- TODO 有時間來新增hover出現icon的功能  20220622 -->
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mx-auto text-center">
            <li class="mx-4 nav-item">
              <router-link class="nav-link link-light" to="/">
                首頁</router-link
              >
            </li>
            <li class="mx-4 nav-item">
              <router-link class="nav-link link-light" to="/about"
                >關於</router-link>
            </li>
            <li class="mx-4 nav-item">
              <router-link class="nav-link link-light" to="/products"
                >比賽周邊</router-link
              >
            </li>
            <li class="mx-4 nav-item">
              <router-link class="nav-link link-light" to="/mineVerse"
                >元宇宙商圈</router-link
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </section>
</template>

<script>
export default {
  mounted() {
    var nav = document.querySelector("nav");
    window.addEventListener("scroll", function () {
      if (this.window.pageYOffset > 50) {
        nav.classList.add("navbarbg");
      } else {
        nav.classList.remove("navbarbg");
      }
    });

    
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
#icon {
  display: none;
}
li {
  font-size: larger;
}
li:hover {
  /* background-color: black; */
  border-bottom: yellow solid;
}
    ul {
        list-style: none;
        margin: 0;
        padding: 0;
    }

.navbarbg{
    transition: .5s;
    background: black;

}

@media handheld,screen and (max-width: 986px){
  nav {
    background: black;
  }
}
</style>
