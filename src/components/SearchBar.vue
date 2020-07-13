<template>
  <div class="main-search-bar">
    <div class="main-search-bar-input">
      <form action class="main-search-bar-form">
        <input class="input" type="text" placeholder="Search for a tip record..." name="search" />
        <button type="submit" class="button-submit">
          <img src="../assets/search.svg" alt />
        </button>
      </form>
    </div>
    <div class="main-search-bar-links">
      <ul>
        <li>
          <a href="#">Latest</a>
        </li>
        <li>
          <a href="#">Most Popular</a>
        </li>
        <li>
          <a href="#">Curators Choice</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>

.main-search-bar {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  margin-bottom: 15px;
  background: #efefef;
  border-bottom: 1px solid darkgray;
  border-radius: 5px 5px 0 0;
  overflow: hidden;
}

.main-search-bar-input,
.main-search-bar-links {
  flex: 0 0 50%;
  max-width: 50%;
}

.main-search-bar-form {
  display: flex;
  flex-wrap: wrap;
  background: #fff;
  border-radius: 5px 5px 0 0;
}

.main-search-bar-form .input {
  flex: 1 0 0;
  padding: 0 10px;
  font-size: 1rem;
  color: #949494;
}

.main-search-bar-form .input::placeholder {
  color: #949494;
  opacity: 1;
}

.main-search-bar-form .input:focus {
  color: #311b58;
}

.main-search-bar-form .input:focus::placeholder {
  color: #fff;
  opacity: 1;
}

.main-search-bar-form .button-submit {
  padding: 10px;
  background: darkgrey;
  border-radius: 0 5px 0 0;
  cursor: pointer;
}

.main-search-bar-links ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;
  padding: 0 20px;
}

.main-search-bar-links ul li {
  margin: 0 10px;
}

.main-search-bar-links ul li:first-child {
  margin-left: 0;
}

.main-search-bar-links ul li:last-child {
  margin-right: 0;
}

.main-search-bar-links ul li a {
  color: #949494;
  font-weight: 500;
  font-size: 0.875rem;
}

.main-search-bar-links ul li a:hover,
.main-search-bar-links ul li a:focus,
.main-search-bar-links ul li a:active {
  color: #ff548d;
}
</style>