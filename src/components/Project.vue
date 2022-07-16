<template>
  <div class="project">
    <img
      :src="require('../assets/images/' + image)"
      alt="Project Image"
      class="project-image"
    />
  </div>
</template>

<script>
export default {
  name: "Project",
  props: ["image"],
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

.project-image {
  width: 100%;
  max-width: 600px;
  max-height: 600px;
  margin: 0 auto;
}

h2 {
  margin: 0;
}
</style>
