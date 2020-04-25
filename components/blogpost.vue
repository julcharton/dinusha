<template>
  <div class="blog-post">
    <!-- <div class="banner">
      <img v-bind:src="banner" />
    </div>-->
    <div class="content">
      <div class="main-title">{{title}}</div>
      <div class="main-subtitle">{{type}}, {{year}}</div>
      <div class="description">
        <p>{{description}}</p>
      </div>
    </div>
    <div v-for="(value, name) in credentials" :key="name">
      <div class="subtitle">{{name}}</div>
      <div class="sub">
        <p v-for="n in value" :key="n">{{n}}</p>
      </div>
    </div>
    <div class="iframe-container">
      <iframe
        :src="`https://player.vimeo.com/video/${videoid}?title=0&byline=0&portrait=0`"
        frameborder="0"
        allow="autoplay; fullscreen"
        allowfullscreen
      ></iframe>
    </div>
  </div>
</template>
<script>
export default {
  mounted() {},
  props: [
    "title",
    "banner",
    "credentials",
    "description",
    "year",
    "type",
    "videoid"
  ]
};
</script>
<style scoped>
.iframe-container {
  overflow: hidden;
  padding-top: 56.25%;
  position: relative;
}

.iframe-container iframe {
  border: 0;
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}
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
  height: 400px;
  object-fit: cover;
}
.blog-post {
}
</style>