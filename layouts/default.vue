<template>
  <div>
    <sidebar />
    <nuxt />
  </div>
</template>
<script>
import sidebar from "@/components/sidebar";
export default {
  components: {
    sidebar
  }
};
</script>
<style>
.container {
  margin: 96px;
  min-height: 100vh;
  display: flex;
  justify-content: start;
  align-items: start;
}
:root {
  font-size: 16px;
  font-family: "Montserrat";
  --text-primary-200: #808080;
  --text-primary-400: #353535;
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
font,
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
td {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
  font-weight: inherit;
  font-style: inherit;
  font-size: 100%;
  font-family: inherit;
  vertical-align: baseline;
  color: inherit;
  text-decoration: inherit;
  cursor: inherit;
}
</style>
