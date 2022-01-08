<template>
  <div class="project">
    <a target="_blank" :href="link">
      <img :src="require('../assets/images/' + image)" alt="Project Image" />
    </a>

    <h2>{{ title }}</h2>
    <p>
      {{ description }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Project",
  props: ["link", "image", "title", "description"],
};
</script>

<style scoped>
.project {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin: 0 auto;
  max-width: 600px;
  padding: 0 20px;
}

h2 {
  margin: 0;
}
</style>
