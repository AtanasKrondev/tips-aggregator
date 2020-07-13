<template>
  <div id="app">
    <app-header></app-header>
    <main class="site-main">
      <div class="container">
        <app-main-content></app-main-content>
        <app-side-content></app-side-content>
      </div>
    </main>

    <app-footer :author="author"></app-footer>
  </div>
</template>

<script>
import AppHeader from "./components/Header";
import AppMainContent from "./components/MainContent";
import AppSideContent from "./components/SideContent";
import AppFooter from "./components/Footer";

export default {
  name: "App",
  components: {
    AppHeader,
    AppMainContent,
    AppSideContent,
    AppFooter
  },
  data() {
    return { author: "Atanas Krondev" };
  }
};
</script>

<style>
/* Resets */

* {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
b,
u,
i,
center,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
embed,
figure,
figcaption,
footer,
header,
hgroup,
menu,
nav,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
  background: transparent;
  font-size: 100%;
  font: inherit;
  text-decoration: none;
  vertical-align: baseline;
}

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
  display: block;
}

html,
body {
  font-size: 16px;
  line-height: 1.5;
  font-family: "Roboto", sans-serif;
  background: #dfdfdf;
}

b,
strong {
  font-weight: 500;
}

ol,
ul {
  list-style: none;
}

blockquote,
q {
  quotes: none;
}

blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

img {
  max-width: 100%;
  height: auto;
  vertical-align: middle;
}

/* Global CSS */

.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 1500px;
  max-width: 100%;
  margin: 0 auto;
}

.container-box-big {
  width: 1000px;
  max-width: 100%;
  padding-right: 20px;
  padding-left: 20px;
}

.container-box-small {
  width: 450px;
  max-width: 100%;
  margin-right: 20px;
  margin-left: 20px;
}

.text-center {
  text-align: center;
}

.text-right {
  text-align: right;
}

.clearfix::before,
.clearfix::after {
  content: "";
  display: block;
}

.clearfix::after {
  clear: both;
}

/* Main */

.main-content,
.main-side-bar {
  padding-top: 2rem;
}
</style>
