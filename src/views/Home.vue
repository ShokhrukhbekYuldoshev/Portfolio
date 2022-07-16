<template>
  <header>
    <div class="overlay">
      <div class="content">
        <h1>Simply The Best</h1>
        <p>
          Hello! I am Shokhrukhbek Yuldoshev, flutter developer from Samarkand,
          Uzbekistan. I am a self-taught developer with a passion for flutter
          and web development.
        </p>
        <br />
        <button @click="handleClick">Read more</button>
      </div>
    </div>
  </header>
</template>

<script>
import { useRouter } from "vue-router";
export default {
  name: "Home",
  setup() {
    const router = useRouter();

    const handleClick = () => {
      router.push("/about");
    };

    return {
      handleClick,
    };
  },
};
</script>

<style scoped>
header {
  text-align: center;
  height: 90vh;
  width: 100%;
  background-size: cover;
  background-attachment: fixed;
  position: relative;
  overflow: hidden;
}
.overlay {
  width: 100%;
  height: 100%;
  padding: 5rem;
  color: var(--white);
  text-shadow: 0.1rem 0.1rem 0.1rem var(--black);
  background-image: linear-gradient(
    135deg,
    rgba(0, 0, 0, 0.8) 10%,
    rgba(0, 0, 0, 1) 100%
  );
}

.content {
  position: absolute;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
  min-width: 60rem;
}

h1 {
  font-size: 8rem;
  margin-bottom: 3rem;
}

p {
  margin-bottom: 3rem;
  font-size: 2rem;
}

@media screen and (max-width: 600px) {
  h1 {
    font-size: 6rem;
  }

  .content {
    min-width: 50rem;
  }

  p {
    font-size: 1.6rem;
  }
}

@media screen and (max-width: 400px) {
  h1 {
    font-size: 5rem;
  }

  .content {
    min-width: 40rem;
  }

  p {
    font-size: 1.5rem;
  }
}

@media screen and (max-width: 350px) {
  .content {
    min-width: 35rem;
  }
  h1 {
    font-size: 4rem;
  }

  p {
    font-size: 1.4rem;
  }
}

@media screen and (max-width: 300px) {
  .content {
    width: 30rem;
  }
  p {
    font-size: 1.3rem;
  }
}
</style>
