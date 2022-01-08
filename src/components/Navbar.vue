<template>
  <div class="nav">
    <div>
      <router-link to="/" class="router-link-active">
        <h3>Yuldoshev</h3>
      </router-link>
    </div>
    <div class="links">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/projects">Projects</router-link>
      <router-link class="cta" to="/contact">Contact</router-link>
    </div>
    <img
      @click="handleClick"
      class="menuBtn"
      :src="require('../assets/images/' + image)"
      alt="menu"
    />
  </div>
  <div class="menu">
    <div class="menu-item">
      <router-link to="/">Home</router-link>
    </div>
    <div class="menu-item">
      <router-link to="/about">About</router-link>
    </div>
    <div class="menu-item">
      <router-link to="/projects">Projects</router-link>
    </div>
    <div class="menu-item cta">
      <router-link to="/contact">Contact</router-link>
    </div>
  </div>
</template>

<script>
import { useRouter } from "vue-router";

export default {
  setup() {
    let image = "menu.png";

    const router = useRouter();
    router.afterEach(() => {
      const menuBtn = document.querySelector(".menuBtn");
      const menu = document.querySelector(".menu");
      const body = document.querySelector("body");
      menuBtn.classList.remove("active");
      menu.style.visibility = "hidden";
      menu.style.opacity = "0";
      body.style.overflow = "visible";
      image = "menu.png";
      menuBtn.src = require("../assets/images/" + image);
    });

    const handleClick = () => {
      const menuBtn = document.querySelector(".menuBtn");
      const menu = document.querySelector(".menu");
      const body = document.querySelector("body");
      menuBtn.classList.toggle("active");

      if (menuBtn.classList.contains("active")) {
        image = "close.png";
        menu.style.visibility = "visible";
        menu.style.opacity = "1";
        body.style.overflow = "hidden";
      } else {
        image = "menu.png";
        menu.style.visibility = "hidden";
        menu.style.opacity = "0";
        body.style.overflow = "visible";
      }
      menuBtn.src = require("../assets/images/" + image);
    };

    return {
      handleClick,
      image,
    };
  },
};
</script>

<style>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-height: 10vh;
  padding: 0rem 12.8rem;
  background: var(--black);
}

.nav-dark {
  background: #000;
}

.links {
  display: flex;
  justify-content: space-between;
  gap: 2rem;
  align-items: center;
}

.cta {
  background: var(--black);
  color: var(--white);
  padding: 0.8rem 1.6rem;
  border-radius: 0.8rem;
  font-size: 1.6rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1rem;
  transition: all 0.2s;
  cursor: pointer;
  border: none;
  outline: none;
  box-shadow: 0 0.2rem 0.4rem rgba(0, 0, 0, 0.2);
  text-decoration: none;
  animation: pulse 1s infinite alternate;
}

.menu {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  height: 100vh;
  background: var(--black);
  display: flex;
  flex-direction: column;
  gap: 2rem;
  justify-content: center;
  align-items: center;
  opacity: 0;
  visibility: hidden;
  transition: all 0.2s;
}

.menu-item {
  padding: 1.6rem;
  font-size: 1.6rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1rem;
  transition: all 0.2s;
  cursor: pointer;
  border: none;
  outline: none;
  box-shadow: 0 0.2rem 0.4rem rgba(0, 0, 0, 0.2);
  text-decoration: none;
}

.menuBtn {
  width: 2.4rem;
  height: 2.4rem;
  cursor: pointer;
  transition: all 0.2s;
  filter: invert(1);
  display: none;
  z-index: 10000;
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

@media screen and (max-width: 1000px) {
  .nav {
    padding: 0rem 6.4rem;
  }
}

@media screen and (max-width: 800px) {
  .nav {
    padding: 0rem 3.2rem;
  }
}

@media screen and (max-width: 600px) {
  .nav {
    padding: 0rem 1.6rem;
  }

  .links {
    gap: 1.6rem;
  }
}

@media screen and (max-width: 500px) {
  .links {
    display: none;
  }

  .menuBtn {
    display: block;
  }
}
</style>
