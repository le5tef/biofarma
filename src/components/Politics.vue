<template>
  <v-row class="politics no-gutters">
    <v-col
      cols="12"
      offset-lg="3"
      lg="7"
      offset-xl="4"
      xl="6"
      class="d-flex align-center justify-center"
    >
      <v-img
        class="rounded-lg"
        :height="$vuetify.breakpoint.mdAndUp ? '500' : '300'"
        src="../assets/storage.jpg"
      ></v-img>
    </v-col>
    <v-col
      cols="12"
      lg="4"
      class="white py-8 py-md-12 py-xl-14 px-8 px-md-14"
      :class="
        $vuetify.breakpoint.name == 'xl' || $vuetify.breakpoint.name == 'lg'
          ? 'politics--text outlined rounded-lg'
          : $vuetify.breakpoint.name == 'md'
          ? 'politics--text-mobile rounded-lg'
          : 'politics--text-mobile underlined'
      "
    >
      <h1 class="underlined politics--title">Качество</h1>
      <div class="mt-3">
        Наша компания заботится о каждом клиенте и контролирует качество всех
        доставляемых товаров и поставляемых нами услуг.
      </div>
      <div class="mt-3">
        В любые погодные условия , в любой день недели ,мы умеем оперативно
        доставить товар в любую точку страны с сохранением терморежима.
      </div>
      <div v-if="showText" class="mt-3">
        С каждым днем нам доверяет больше клиентов и производителей,а значит мы
        расширяем географию продаж.
      </div>

      <div v-if="showText" class="mt-3">
        Ежегодно Биофарма расширяет прайс -лист и открывает новые регионы
        поставок..
      </div>
      <div v-if="showText" class="mt-3">
        В рамках борьбы с COVID наша компания осуществили поставки
        противовирусных препаратов в более чем 10 регионов РФ .
      </div>
      <v-btn
        v-if="!showText"
        outlined
        class="mt-4"
        color="rgb(50 186 71)"
        @click="showText = true"
        >Подробнее</v-btn
      >
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      showText: false,
    };
  },
};
</script>

<style lang='scss' scoped>
.politics {
  position: relative;
  &--text {
    position: absolute;
    z-index: 3;
    top: 50%;
    left: 15%;
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
    transform: translate(-50%, -50%);
  }
  &--title {
    font-weight: 700;
    width: fit-content !important;
  }
}
</style>