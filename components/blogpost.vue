<template>
  <div class="blog-post">
    <div class="banner">
      <img v-bind:src="banner" />
    </div>
    <div class="content">
      <div class="main-title">{{title}}</div>
      <div class="main-subtitle">Feature Film, 2017</div>
      <div class="description">
        <p>A heartwarming tale about a young female farmer, whose imaginary friend of the last 20 years only realizes he is in love with her when she starts to fall for a real man. Unable to face losing her, he must fight to become real himself.</p>
      </div>
    </div>
    <div v-for="(value, name) in credentials" :key="name">
      <div class="subtitle">{{name}}</div>
      <div class="sub">
        <p v-for="n in value" :key="n">{{n}}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: String,
    banner: String,
    credentials: Object
  }
};
</script>
<style scoped>
.subtitle {
  margin-bottom: 6px;
}
.sub {
  margin-bottom: 24px;
}
p {
  font-size: 14px;
  font-weight: 400;
  font-family: "Playfair Display";
  letter-spacing: 0.9px;
  color: var(--text-primary-200);
  display: inline;
}
.description {
  margin: 16px 0 24px 0;
}
.main-title {
  font-size: 24px;
  margin-top: 24px;
  margin-bottom: 6px;
}
.main-subtitle {
  font-size: 14px;
  color: var(--text-primary-200);
}
.banner img {
  width: 100%;
  height: 385px;
  object-fit: cover;
}
.blog-post {
}
</style>