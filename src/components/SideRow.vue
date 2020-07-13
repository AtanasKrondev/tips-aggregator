<template>
  <div class="aside">
    <a href="#" class="aside-tag">Topic {{article.id}}</a>
    <div class="aside-box">
      <app-side-card v-for="card in article.articles" :key="card"></app-side-card>
    </div>
  </div>
</template>

<script>
import AppSideCard from "./SideCard";
export default { components: { AppSideCard }, props: { article: Object } };
</script>

<style scoped>
.aside {
  position: relative;
  background: #fff;
  margin-bottom: 20px;
  padding: 20px;
  border-radius: 5px;
}

.aside:last-of-type {
  margin-bottom: 0;
}

.aside-tag {
  z-index: 1;
  position: absolute;
  top: 0;
  left: 0;
  padding: 0 10px;
  background: #fff;
  border: 1px solid;
  color: #311b58;
  font-weight: 500;
  font-size: 0.9rem;
  border-radius: 5px;
}

.aside-tag:hover,
.aside-tag:focus,
.aside-tag:active {
  color: #ff548d;
}

.aside-box {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>