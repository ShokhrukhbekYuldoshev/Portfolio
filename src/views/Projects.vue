<template>
  <h1>My latest projects</h1>
  <h2>Nilu Mobile POS - Easily manage your sales, income and products</h2>
  <div class="projects">
    <Project image="nilu/present-1.png" />
    <Project image="nilu/present-2.png" />
    <Project image="nilu/present-3.png" />
    <Project image="nilu/present-4.png" />
    <Project image="nilu/present-5.png" />
    <Project image="nilu/present-6.png" />
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

h2 {
  text-align: center;
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
