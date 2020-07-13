<template>
  <footer class="site-footer text-center">
    App by
    <strong>{{author}}</strong>
    :)
  </footer>
</template>

<script>
export default {
  props: { author: String }
};
</script>

<style scoped>
.site-footer {
  padding: 10px;
  color: #311b58;
}

.site-footer strong {
  color: #ff548d;
}
</style>