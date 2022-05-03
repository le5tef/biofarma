<template>
  <div id="aboutUs">
    <!-- <Carousel
      id="carousel"
      :class="active.includes('carousel') ? activeClasses : notActiveClasses"
    /> -->
    <Video />
    <Benefits id="benefits" />

    <Sales id="sales" />
    <Goods id="goods" />
    <Politics id="politics" class="mb-4" />
    <License id="license" />
    <News id="news" />
  </div>
</template>

<script>
import Goods from "../components/Goods.vue";
import Video from "../components/Video.vue";
import Benefits from "../components/Benefits.vue";
import Sales from "../components/Sales.vue";
import Politics from "../components/Politics.vue";
import License from "../components/License.vue";
import News from "../components/News.vue";
import { eventBus } from "../main";
// import { eventBus } from "../main";
export default {
  data() {
    return {};
  },
  methods: {
    scrollTo(component) {
      let element = document.getElementById(component);
      element.scrollIntoView({
        block: this.$vuetify.breakpoint.mdAndUp ? "center" : "start",
        behavior: "smooth",
      });
    },
  },
  created() {
    eventBus.$on("scroll-to-element", (x) => {
      this.scrollTo(x.component);
    });
  },
  components: {
    Video,
    Goods,
    News,
    Benefits,
    Sales,
    Politics,
    License,
  },
};
</script>

<style>
.active {
  opacity: 1 !important;
}
.non_active {
  opacity: 0 !important;
}
</style>