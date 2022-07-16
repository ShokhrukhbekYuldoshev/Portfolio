<template>
  <h1>About me</h1>
  <div class="about">
    <img src="../assets/images/logo.jpg" alt="" />
    <div class="about__content">
      <p>
        Hello! I am Shokhrukhbek Yuldoshev,
        <strong>flutter developer</strong> from Samarkand, Uzbekistan. I am a
        self-taught developer with a passion for
        <strong>flutter and web development</strong>. I have a strong background
        in development and have experience in building mobile, desktop and web
        applications using
        <strong
          >Dart(Flutter), Vue.js, React.js, Node.js, Django, SQL,
          Firebase</strong
        >
        and <strong>MongoDB</strong>.
      </p>
      <a class="btn cta" @click="handleClick">Hire me</a>
    </div>
  </div>
</template>

<script>
import { useRouter } from "vue-router";
export default {
  setup() {
    const router = useRouter();

    const handleClick = () => {
      router.push("/contact");
    };
    return {
      handleClick,
    };
  },
};
</script>

<style scoped>
.about {
  display: flex;
  gap: 4.8rem;
  justify-content: center;
  align-items: flex-start;
  padding: 0 16.4rem;
}

.about__content {
  width: 60%;
}

.btn {
  display: inline-block;
  margin-top: 1rem;
  opacity: 1 !important;
}

img {
  width: 25.6rem;
}

p {
  font-size: 1.8rem;
  line-height: 2;
}

@media screen and (max-width: 1000px) {
  .about {
    padding: 0 6.4rem;
  }
}

@media screen and (max-width: 800px) {
  .about {
    padding: 0 3.2rem;
    flex-direction: column;
    align-items: center;
  }

  p {
    font-size: 1.6rem;
    line-height: 1.8;
  }
}

@media screen and (max-width: 600px) {
  .about__content {
    width: 80%;
  }
  .about {
    padding: 0 1.6rem;
  }

  img {
    width: 20.8rem;
  }
}
</style>
