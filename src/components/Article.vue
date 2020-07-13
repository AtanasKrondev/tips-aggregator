<template>
  <div class="article">
    <div class="article-content content">
      <div class="article-content-header">
        <div class="article-content-header-btns">
          <a href="#" class="btn-link btn-link-like">
            <img src="../assets/heart.svg" alt="Like Button Icon" />
          </a>
          &nbsp;
          <a href="#" class="btn-link btn-link-comment">
            <img src="../assets/chat.svg" alt="Chat Button Icon" />
          </a>
        </div>
        <div class="article-content-title">
          <h2>{{tip.title}}</h2>
        </div>
      </div>
      <div class="article-content-main">
        <p>
          <a :href="tip.url">{{tip.url}}</a>
        </p>
      </div>
      <div class="article-content-footer">
        <span class="article-info article-date">{{tip.timestamp | toDate}}</span>
        <span class="article-info article-user">
          <strong class="article-user-rating">+{{tip.amount_ae}} AE</strong>
          by
          <strong class="article-user-name">{{tip.sender | shortenName}}</strong>
        </span>
        <span class="article-info article-likes">
          <img src="../assets/heart.svg" alt />
          {{tip.total_claimed_amount}}
          <strong
            class="article-likes-rating"
          >+{{tip.total_unclaimed_amount}} AE</strong>
        </span>
        <span class="article-info article-comments">
          <img src="../assets/chat.svg" alt />
          {{tip.commentCount}}
        </span>
        <span class="article-source">
          <a href="#" class="link article-source-link">
            <img src="../assets/facebook.svg" alt />&nbsp;Facebook
          </a>
        </span>
      </div>
    </div>
    <div class="article-content preview clearfix">
      <h2>{{tip.preview.title}}</h2>
      <img
        class="align-image"
        :src="`https://raendom-backend.z52da5wt.xyz${tip.preview.image}`"
        :alt="tip.preview.title"
      />
      <p class="align-text">{{tip.preview.description}}</p>
    </div>
  </div>
</template>

<script>
import moment from "moment";
export default {
  props: {
    tip: Object
  },
  filters: {
    toDate(timestamp) {
      return moment.unix(timestamp / 1000).format("MM/DD/YYYY hh:mm A");
    },
    shortenName(name) {
      if (name.length > 21) {
        return `${name.slice(0, 10)}...${name.slice(-8)}`;
      } else return name;
    }
  }
};
</script>

<style scoped>
.article {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  max-width: 100%;
  margin-bottom: 15px;
  background: #fff;
  border-radius: 5px;
  overflow: hidden;
}

.article:last-of-type {
  margin-bottom: 0;
}

.article-content {
  position: relative;
}

.article-content.content {
  display: flex;
  flex-direction: column;
  flex: 0 0 70%;
  max-width: 70%;
}

.article-content.preview {
  flex: 0 0 30%;
  max-width: 30%;
  padding: 5px 10px;
  border-left: 1px solid #d9d9d9;
}

.article-content.preview::before {
  content: "";
  position: absolute;
  top: 50%;
  left: -16px;
  transform: translateY(-50%);
  width: 17px;
  height: 24px;
  background: url("../assets/arrow.png") no-repeat 0 0;
}

.article-content-header {
  display: flex;
  flex-wrap: wrap;
  flex: 0 0 auto;
  padding: 5px 50px 5px 10px;
}

.article-content-header-btns {
  flex: 0 0 auto;
  margin-top: 5px;
  margin-right: 10px;
}

.article-content-title {
  flex: 1 0 0;
}

.btn-link {
  display: inline-block;
  padding: 4px 8px;
  background: #f1f1f1;
}

.btn-link img {
  width: 20px;
}

.article-content-title h2 {
  color: #4d4d4d;
  font-weight: 500;
  font-size: 0.9375rem;
}

.article-content-main {
  flex: 1 0 auto;
  padding: 5px 50px 5px 10px;
}

.article-content-main p {
  font-size: 0.75rem;
}

.article-content-main a {
  color: #311b58;
}

.article-content-main a:hover,
.article-content-main a:focus,
.article-content-main a:active {
  text-decoration: underline;
}

.article-content-footer {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  flex-shrink: 0;
  padding: 2px 10px;
  background: #f1f1f1;
}

.article-info {
  margin-right: 20px;
  color: #949494;
  font-size: 0.75rem;
}

.article-date {
  margin-right: 5px;
}

.article-user .article-user-rating,
.article-likes .article-likes-rating {
  color: #ff548d;
  font-weight: 500;
}

.article-user .article-user-name {
  color: #311b58;
  font-weight: 500;
}

.article-source {
  margin-left: auto;
}

.article-source .link {
  color: #311b58;
  font-size: 0.75rem;
  font-weight: 500;
}

.article-content.preview h2 {
  margin-bottom: 5px;
  color: #4d4d4d;
  font-size: 0.8125rem;
  font-weight: 500;
}

.article-content.preview .align-image {
  float: left;
  margin-right: 10px;
  margin-bottom: 5px;
  width: 120px;
  height: auto;
}

.article-content.preview p {
  color: #2e2e2e;
  font-size: 0.75rem;
  overflow-wrap: break-word;
}
</style>