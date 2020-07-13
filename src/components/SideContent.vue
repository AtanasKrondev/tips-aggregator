<template>
  <div class="container-box-small main-side-bar">
    <div class="main-side-bar-frame">
      <app-side-row v-for="article in sideArticles" :key="article.id" :article="article"></app-side-row>
    </div>
    <app-side-footer></app-side-footer>
  </div>
</template>

<script>
import AppSideRow from "./SideRow";
import AppSideFooter from "./SideFooter";
export default {
  components: { AppSideRow, AppSideFooter },
  data() {
    return {
      sideArticles: [
        { id: 1, articles: [1, 2, 3] },
        { id: 2, articles: [1, 2, 3] },
        { id: 3, articles: [1, 2, 3] },
        { id: 4, articles: [1, 2, 3] },
        { id: 5, articles: [1, 2, 3] },
        { id: 6, articles: [1, 2, 3] },
        { id: 7, articles: [1, 2, 3] }
      ]
    };
  }
};
</script>

<style scoped>
/* Side bar */

.main-side-bar {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
  background: #efefef;
}

.main-side-bar-frame {
  width: 100%;
  height: 100vh;
  padding: 0 20px;
  overflow-y: auto;
}

.main-side-bar-frame::-webkit-scrollbar {
  width: 6px;
}

.main-side-bar-frame::-webkit-scrollbar-track {
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
}

.main-side-bar-frame::-webkit-scrollbar-thumb {
  background-color: darkgrey;
  outline: 1px solid slategrey;
}
</style>