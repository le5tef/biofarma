<template>
  <v-row class="sales no-gutters mt-8">
    <v-col
      cols="12"
      offset-lg="2"
      lg="7"
      offset-xl="2"
      xl="6"
      class="d-flex align-center justify-center"
    >
      <v-img
        class="rounded-lg"
        :height="$vuetify.breakpoint.mdAndUp ? '500' : '300'"
        src="../assets/farm.jpg"
      ></v-img>
    </v-col>
    <v-col
      cols="12"
      lg="4"
      class="white py-12 py-xl-16 px-12"
      :class="
        $vuetify.breakpoint.name == 'xl' || $vuetify.breakpoint.name == 'lg'
          ? 'sales--text outlined rounded-lg'
          : $vuetify.breakpoint.name == 'md'
          ? 'sales--text-mobile rounded-lg'
          : 'sales--text-mobile underlined'
      "
    >
      <h1 class="underlined sales--title">Продажи</h1>
      <div class="mt-3">
        Ежедневно изучая рынок, действуя в интересах клиентов, мы постоянно
        совершенствуем не только логистику и хранение, но и динамично
        увеличиваем объёмы продаж !
      </div>
      <div class="mt-3">
        Мы являемся лидерами в сегменте продаж иммунобиологических препаратов,
        но не ограничиваемся этим.
      </div>
    </v-col>
  </v-row>
</template>

<style lang='scss' scoped>
.sales {
  position: relative;
  &--text {
    position: absolute;
    z-index: 3;
    top: 50%;
    left: 50%;
    transform: translateY(-50%);

    box-shadow: 0px 0px 13px 0px rgba(34, 60, 80, 0.2);
  }
  &--text-mobile::after {
    content: "";
    position: absolute;
    z-index: 3;
    top: 100%;
    left: 50%;
    width: 90vw;
    height: 300px;
    transform: translate(-50%, -50%);
  }
  &--title {
    font-weight: 700;
    width: fit-content;
  }
}
</style>