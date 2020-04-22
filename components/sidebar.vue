<template>
  <div class="sidebar">
    <h1 class="title">{{ name }}</h1>
    <h1 class="title">{{ surname }}</h1>

    <div class="category" v-for="menu in menus" :key="menu">
      <h2 class="categorie-title">{{menu.title}}</h2>
      <div class="categorie-item" v-for="subtitle in menu.subtitles" :key="subtitle">
        <a v-bind:href="subtitle.route">{{subtitle.name}}</a>
      </div>
    </div>
    <div class="category link">
      <nuxt-link to="/about">
        <h2 class="categorie-title">About</h2>
      </nuxt-link>
    </div>
  </div>
</template>
<script>
import Vue from "vue";
export default Vue.extend({
  data() {
    return {
      name: "Dinusha",
      surname: "RATNAWEERA",
      menus: [
        {
          title: "Filmography",
          subtitles: [
            { name: "The pretend One - 2017", route: "#thePretendOne" },
            { name: "Legacy - 2016", route: "legacy" }
          ]
        },
        {
          title: "Commercial",
          subtitles: [
            { name: "Be Okinawa - 2017", route: "#beOkinawa" },
            { name: "Jake & Kayla - 2017", route: "#jakeAndKayla" },
            { name: "Meditasting - 2015", route: "#meditasting" },
            { name: "Crash The Superbowl - 2015", route: "#crashTheSuperbowl" },
            {
              name: "Everyday Australian Mornings - 2015",
              route: "/everydayAustralianMornings"
            },
            { name: "Beer Dance - 2011", route: "/beerDance" }
          ]
        }
      ]
    };
  }
});
</script>
<style scoped>
a {
  cursor: pointer;
}
.category {
  margin-top: 42px;
}
.categorie-title {
  margin-bottom: 14px;
}
.categorie-item {
  cursor: pointer;
  display: table;
  color: var(--text-primary-200);
  margin-bottom: 8px;
}
.categorie-item:hover {
  color: var(--text-primary-400);
  border-bottom: 1px solid var(--text-primary-400);
}
.title {
  font-family: "Montserrat";
  font-weight: 400;
  font-size: 36px;
  color: var(--text-primary-400);
}

.sidebar {
  width: 17rem;
  height: calc(100vh - 96px);
  position: fixed;
}
</style>
