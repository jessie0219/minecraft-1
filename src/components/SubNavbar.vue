<template>
  <section>
    <div class="container-fluid">
      <div class="row d-flex flex-column text-center">
        <div class="col sticky" id="navbar">
          <div class="burger p-3">
            <i class="bi bi-list"></i>
          </div>
          <nav class="main-nav">
            <ul class="col menu overflow-hidden fs-3">
              <li><router-link to="/">首頁</router-link></li>
              <li><router-link to="/about">關於</router-link></li>
              <li><router-link to="/products">比賽周邊</router-link></li>
              <li><router-link to="/mineVerse">元宇宙商圈</router-link></li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </section>
  <router-view />
</template>

<script>
export default {
  name: "SubNavbar",
};
</script>

<style scoped>
nav ul {
  display: flex;
  justify-content: center;
  overflow: hidden;
}

nav a {
  display: inline-block;
  width: 200px;
  height: 70px;
  padding: 15px 0 15px 0;
  color: black;
}

nav a:hover {
  color: black;
  border-bottom: 3px solid yellow;
}

.burgar {
  color: white;
  font-size: 1.5rem;
  display: none;
}

.sticky {
  position: fixed;
  top: 0;
  background: rgba(0, 0, 0, 0.7);
  transition: 1s;
  z-index: 1;
}

.sticky a {
  color: white;
}

.sticky a:hover {
  color: white;
}

@media handheld, screen and (max-width: 786px) {
  .burger {
    display: block;
    float: right;
  }

  .showing {
    max-height: 15em;
    margin-top: 50px;
  }

  #navbar {
    background: rgba(0, 0, 0, 0.7);
    position: fixed;
  }

  nav a {
    color: white;
  }

  nav a:hover {
    color: white;
    border-bottom: 3px solid yellow;
  }

  nav ul {
    color: white;
    flex-direction: column;
    align-self: flex-end;
    max-height: 0px;
    transition: 1s;
    padding-left: 50px;
  }

  nav ul li {
    box-sizing: border-box;
    width: 100%;
    text-align: center;
  }
}
</style>
