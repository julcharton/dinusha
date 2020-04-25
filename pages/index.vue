<template>
  <div class="main">
    <h1>Dinusha RATNAWEERA</h1>
    <p>producer</p>
    <span class="vertical-line"></span>
    <nuxt-link class="link" to="/thePretendOne">Portfolio</nuxt-link>
  </div>
</template>
<style scoped>
.link:hover {
  cursor: pointer;
  border-bottom: 1px solid black;
}
h1 {
  font-size: 24px;
  margin-bottom: 8px;
}
p {
  color: var(--text-primary-200);
}
.main {
  margin-left: 17rem;
  padding: 0 0 0 6rem;
  display: flex;
  align-content: center;
  height: calc(100vh - 96px - 96px);
  margin: 0 auto;
  text-align: center;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.vertical-line {
  display: inline-block;
  border-left: 1px solid #ccc;
  margin: 8px 10px;
  height: 100px;
}
</style>