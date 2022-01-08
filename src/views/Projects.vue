<template>
  <h1>My projects</h1>
  <div class="projects">
    <Project
      link="https://incredible-music.web.app/"
      image="incredible-music.png"
      title="Incredible Music"
      description="A music app that allows you to create your own playlist. You can also add songs to your playlist. Used Vue.js and Firebase."
    />
    <Project
      link="https://vue-blog-5f76d.web.app/"
      image="vue-chat.png"
      title="Vue Chat"
      description="A realtime chat app that allows you to chat with other users. Used Vue.js and Firebase."
    />
    <Project
      link="https://incredible-storybooks.herokuapp.com/"
      image="storybooks.png"
      title="Storybooks"
      description="A storybook app that allows you to create your own stories and share them with other users. Used Node.js, Express, MongoDB and Google OAuth."
    />
    <Project
      link="https://incredible-storybooks.herokuapp.com/"
      image="chatcuarto.png"
      title="Chatcuarto"
      description="A chat room app that allows you to chat with other users. Used Node.js, Express, MongoDB."
    />
  </div>
</template>

<script>
import Project from "../components/Project.vue";
export default {
  components: {
    Project,
  },
};
</script>

<style scoped>
h1 {
  margin-bottom: 3rem;
}

.projects {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 4.8rem;
  margin-bottom: 4.8rem;
}
</style>
