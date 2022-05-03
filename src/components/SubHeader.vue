<template v-slot:extension>
  <div>
    <v-app-bar
      class="header"
      height="80"
      :collapse="!$vuetify.breakpoint.mdAndUp && !collapse"
      elevate-on-scroll
      :class="
        !$vuetify.breakpoint.mdAndUp && !collapse
          ? 'd-flex align-center justify-center rounded-br-xl'
          : 'pr-5'
      "
      color="rgb(255 255 255 / 50%)"
    >
      <v-tabs
        color="black"
        centered
        v-if="collapse || $vuetify.breakpoint.mdAndUp"
      >
        <v-tab class="tab" :to="{ name: 'AboutUs' }">О нас</v-tab>
        <v-tab
          v-if="$route.path == '/about-us'"
          @click="scrollTo('goods')"
          class="tab"
          >Продукция</v-tab
        >
        <v-tab
          v-if="$route.path == '/about-us'"
          @click="scrollTo('license')"
          class="tab"
          >Лицензирование</v-tab
        >
        <v-tab
          v-if="$route.path == '/about-us'"
          @click="scrollTo('news')"
          class="tab"
          >Новости</v-tab
        >
        <v-tab class="tab" :to="{ name: 'Contacts' }">Контакты</v-tab>
      </v-tabs>
      <v-btn
        v-if="!$vuetify.breakpoint.mdAndUp"
        @click="collapse = !collapse"
        icon
        ><v-icon>mdi-menu</v-icon></v-btn
      >
    </v-app-bar>
  </div>
</template>

<script>
import { eventBus } from "../main";
export default {
  data() {
    return {
      collapse: false,
    };
  },
  methods: {
    scrollTo(component) {
      eventBus.$emit("scroll-to-element", { component });
      this.collapse = false;
    },
  },
};
</script>

<style scoped>
.header {
  position: fixed;
  top: -1px;
  z-index: 7;
  flex: 0;
}

.tab {
  font-size: 1.25rem !important;
  font-weight: 400;
  line-height: 2rem;
  letter-spacing: 0.0125em !important;
  font-family: system-ui;
}
</style>