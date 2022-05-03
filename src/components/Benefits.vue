<template>
  <v-row class="benefits no-gutters wrapper d-flex pa-4 mt-md-10">
    <v-col cols="12" offset-md="2" md="10" class="mb-md-10 px-4 px-md-0">
      <div class="benefits--title underlined">О компании</div>
    </v-col>
    <v-col
      cols="12"
      offset-md="2"
      md="4"
      class="benefits--subtitle mt-8 mt-md-0 px-4 px-md-0 pr-md-8"
    >
      Уже свыше 10 лет, Био-фарма является надежным поставщиком
      медикаментов,расходных материалов и компонентов крови в лечебные
      учреждения системы здравоохранения Российской федерации.
      <br /><br />Компания обладает современными складскими мощностями , общей
      площадью 2000 квадратных метров ,работающим по GDP стандартам.
      <br /><br />Для удобства клиентов, склады находятся в Москве и Московской
      области. <br /><br
    /></v-col>
    <v-col
      cols="12"
      md="4"
      class="benefits--subtitle mt-4 mt-md-0 px-4 px-md-0 pl-md-8"
      >Био-фарма обладает собственным парком современных рефрижераторов ,на
      каждом из которых своевременно проводится картирование. <br />Все это
      гарантирует оперативность и неизменно высокое качество сервиса доставки
      препаратов до получателей. Ответственными и квалифицированными работниками
      склада ,ежедневно производятся отгрузки во все регионы России,с
      соблюдением всех необходимых условий доставки-вовремя и в срок.
      <br /><br />
      Мы -Био-фарма ! Ваш надежный поставщик лекарственных средств.</v-col
    >
  </v-row>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang='scss' scoped>
.wrapper {
  overflow: auto;
  display: flex;
  width: 100%;
}
.benefits {
  &--title {
    font-size: 40px;
    font-weight: 700;
    width: fit-content;
  }
  &--subtitle {
    font-size: 20px;
    font-weight: 300;
  }
}
</style>