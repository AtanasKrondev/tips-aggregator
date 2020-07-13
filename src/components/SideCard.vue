<template>
  <div class="aside-content">
    <p class="aside-img-box">
      <img src="../assets/Image-1.png" alt />
      <span class="aside-rating">+1500 AE</span>
    </p>
    <p class="aside-like-comment-source-box">
      <span class="aside-info aside-like">
        <img src="../assets/heart.svg" alt />&nbsp;1K
      </span>
      <span class="aside-info aside-comment">
        <img src="../assets/chat.svg" alt />&nbsp;10K
      </span>
      <span class="aside-source">
        <img src="../assets/facebook.svg" alt />
      </span>
    </p>
    <p class="aside-content-box">
      Are We Going To The Moon: Per Aspera Ad Astra
      Or An Example Of...
    </p>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.aside-content {
  flex: 0 0 30%;
  max-width: 30%;
}

.aside-img-box {
  position: relative;
  margin-bottom: 10px;
}

.aside-img-box .aside-rating {
  position: absolute;
  bottom: 0;
  left: 0;
  padding: 0 10px;
  background: #fff;
  color: #ff548d;
  font-size: 0.75rem;
  border-radius: 2px;
}

.aside-like-comment-source-box {
  margin-bottom: 10px;
}

.aside-info {
  margin-right: 10px;
  color: #949494;
  font-size: 0.75rem;
}

.aside-content-box {
  color: #311b58;
  font-size: 0.8125rem;
  font-weight: 500;
}
</style>