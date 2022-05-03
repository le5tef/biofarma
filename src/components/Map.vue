<template>
  <v-col md="12" cols="12" offset-md="0">
    <iframe
      src="https://yandex.ru/map-widget/v1/-/CCUB6WQDLD"
      :width="sizes.width"
      :style="
        $vuetify.breakpoint.mdAndUp
          ? 'min-height: calc(100vh )'
          : 'min-height: calc((100vh ) / 1.8)'
      "
      allowfullscreen="true"
      style="position: relative; border: none; margin-bottom: -7px"
    ></iframe>
  </v-col>
  <!-- <v-col
    cols="12"
    lg="4"
    md="4"
    offset-md="7"
    offset-xl="6"
    class="d-flex align-center flex-column mt-10"
  >
    <div
      class="underlined mt-16 mb-4"
      style="font-size: 34px; font-weight: 300"
    >
      Бизнес-центр
    </div>
    <v-img
      :height="$vuetify.breakpoint.mdAndUp ? '650' : '350'"
      width="100%"
      src="../assets/buissness.jpg"
    />
  </v-col> -->
</template>
<script>
export default {
  computed: {
    sizes() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return {
            width: "100%",
            height: window.innerHeight / 1.5,
          };
        case "sm":
          return {
            width: "100%",
            height: window.innerHeight / 1.5,
          };
        case "md":
          return {
            width: "120%",
            height: window.innerHeight,
          };
        default:
          return {
            width: "120%",
            height: window.innerHeight,
          };
      }
    },
  },
};
</script>