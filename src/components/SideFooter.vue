<template>
  <div class="main-side-bar-footer">
    <p class="copyright">© 2020 Raendom.com</p>
    <ul class="useful-links">
      <li>
        <a href="#">Terms</a>
      </li>
      <li>
        <a href="#">Privacy Policy</a>
      </li>
      <li>
        <a href="#">Cookies</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.main-side-bar-footer {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  padding: 10px 20px;
}

.copyright {
  color: #949494;
  font-size: 0.75rem;
}

.useful-links {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.useful-links li {
  margin: 0 10px;
}

.useful-links li:first-child {
  margin-left: 0;
}

.useful-links li:last-child {
  margin-right: 0;
}

.useful-links li a {
  color: #949494;
  font-size: 0.75rem;
}

.useful-links li a:hover,
.useful-links li a:focus,
.useful-links li a:active {
  text-decoration: underline;
}
</style>