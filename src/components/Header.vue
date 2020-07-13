<template>
  <header class="site-header">
    <div class="container">
      <div class="container-box-big header-left">
        <div class="site-logo-nav-box">
          <a href="/" title="Logo Here" class="site-logo">
            <img src="../assets/TipTokenLogo.svg" alt="Site Logo" />
          </a>
          <nav class="site-navigation">
            <ul class="static">
              <li class="static selected">
                <a href="#">Home</a>
              </li>
              <li class="static">
                <a href="#">Blockchain</a>
              </li>
              <li class="static">
                <a href="#">Gaming</a>
              </li>
              <li class="static">
                <a href="#">Community</a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="site-tips-links-box">
          <a href="#" class="tips-link">
            <img src="../assets/claim.svg" alt="Claim Tips Icon" />&nbsp;&nbsp;Claim Tips
          </a>
          <a href="#" class="tips-link disabled">
            <img src="../assets/heart.svg" alt="Send Tips Icon" />&nbsp;&nbsp;Send Tips
          </a>
          <a href="#" class="tips-link">
            <span class="has-border">
              <img src="../assets/heart.svg" alt="Get Tokens Icon" />
            </span>&nbsp;&nbsp;Get Tokens
          </a>
        </div>
      </div>
      <div class="container-box-small header-right text-right">
        <a href="#" class="hd-right-icon help-icon">
          <img src="../assets/help.svg" alt="Help Icon" />
        </a>
        <a href="#" class="hd-right-icon bell-icon">
          <img src="../assets/bell.svg" alt="Bell Icon" />
        </a>
        <a href="#" class="hd-right-icon user-icon">
          <img src="../assets/user.png" alt="User Icon" />
        </a>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
.site-header {
  position: relative;
  width: 100%;
  background: #fff;
  box-shadow: 0 2px 3px #00000026;
}

.header-left {
  display: flex;
  flex-wrap: wrap;
}

.site-logo-nav-box,
.site-tips-links-box {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  flex: 0 0 50%;
  max-width: 50%;
}

.site-logo-nav-box {
  justify-content: space-between;
}

.site-tips-links-box {
  justify-content: flex-end;
}

/* Navigation */

ul.static {
  display: flex;
  flex-wrap: wrap;
}

li.static {
  margin: 0 15px;
}

li.static:first-child {
  margin-left: 0;
}

li.static:last-child {
  margin-right: 0;
}

li.static > a {
  display: inline-block;
  border-top: 4px solid transparent;
  border-bottom: 4px solid transparent;
  padding: 20px 0;
  color: #311b58;
  font-size: 1.25rem;
}

li.static:hover > a,
li.static:focus > a,
li.static:active > a,
li.static.selected > a {
  color: #ff548d;
}

li.static.selected > a {
  border-bottom-color: #ff548d;
}

/* Tips */

.tips-link {
  display: inline-block;
  width: 140px;
  max-width: 100%;
  margin: 8px;
  padding: 8px;
  background: #f1f1f1;
  color: #311b58;
  text-align: center;
  border-radius: 5px;
}

.tips-link:first-of-type {
  margin-left: 0;
}

.tips-link:last-of-type {
  margin-right: 0;
}

.tips-link .has-border {
  display: inline-block;
  padding: 1px 4px;
  background: #fff;
  border: 1px solid #ff548d;
  border-radius: 50%;
  line-height: 1;
}

.tips-link .has-border img {
  width: 10px;
}

/* Header right icons */

.hd-right-icon {
  display: inline-block;
  margin: 5px;
}

.hd-right-icon:first-of-type {
  margin-left: 0;
}

.hd-right-icon:last-of-type {
  margin-right: 0;
}
</style>