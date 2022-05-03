<template>
  <v-row class="no-gutters my-7 pa-4">
    <v-col cols="12" md="8" offset-md="2">
      <v-carousel
        cycle
        :height="
          $vuetify.breakpoint.name == 'xl'
            ? '620'
            : $vuetify.breakpoint.name == 'lg'
            ? '600'
            : $vuetify.breakpoint.name == 'md'
            ? '500'
            : $vuetify.breakpoint.name == 'sm'
            ? '400'
            : '300'
        "
        class="rounded outlined"
        hide-delimiter-background
        show-arrows-on-hover
      >
        <v-carousel-item v-for="(slide, i) in slides" :src="slide.src" :key="i">
          <v-row class="fill-height no-gutters" align="center">
            <v-col cols="4" offset="2" md="4" lg="3" class="d-flex flex-column">
            </v-col>
          </v-row>
        </v-carousel-item>
      </v-carousel>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data() {
    return {
      slides: [
        {
          title: "10 лет на рынке",
          subtitle:
            "Свыше 10 лет, мы помогаем Российской системе здравоохранения оперативными поставками препаратов крови ,антибиотиков, анестезиологии и лечебного питания.",
          src: require("../assets/1.jpg"),
        },
      ],
    };
  },
};
</script>

<style scoped>
.title {
  background: linear-gradient(
    270deg,
    rgba(52, 170, 73, 1) 0%,
    rgba(118, 187, 98, 0.6671043417366946) 33%,
    rgba(216, 235, 205, 0.3309698879551821) 67%,
    rgba(255, 255, 255, 0) 100%
  );
}
</style>