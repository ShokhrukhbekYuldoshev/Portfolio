<template>
  <footer class="footer">
    <p>Created by <span class="name">Shokhrukhbek Yuldoshev</span></p>
    <div class="social-icons">
      <a href="https://github.com/ShokhrukhbekYuldoshev" target="_blank">
        <i class="fa-brands fa-github"></i>
      </a>
      <a href="https://t.me/therealfreedom" target="_blank">
        <i class="fa-brands fa-telegram"></i>
      </a>
      <a href="https://twitter.com/ShokhrukhbekY" target="_blank">
        <i class="fa-brands fa-twitter"></i>
      </a>
      <a href="https://www.facebook.com/shokhrukhbek.yuldoshev" target="_blank">
        <i class="fa-brands fa-facebook"></i>
      </a>
      <a href="https://www.instagram.com/shokhrukhbekyuldoshev" target="_blank">
        <i class="fa-brands fa-instagram"></i>
      </a>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
.footer {
  background-color: var(--black);
  padding: 20px 0;
  text-align: center;
  color: #fff;
  min-height: 10vh;
}
.social-icons {
  display: flex;
  margin: 1rem auto 0;
  width: 20rem;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  align-items: center;
}

.fa-brands {
  transition: all 0.2s ease-in-out;
  font-size: 2rem;
}

.fa-brands:hover {
  transform: scale(1.2);
  color: #fff;
}

a {
  opacity: 1 !important;
}

.name {
  font-weight: 500;
  transform: scale(1.2);
}
</style>
