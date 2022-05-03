<template>
  <v-col
    cols="12"
    offset="0"
    offset-lg="1"
    md="6"
    lg="5"
    xl="4"
    :style="contactsPosition.style"
    class="pa-4 px-sm-10 py-sm-16 white contants-wrapper"
  >
    <v-container>
      <div class="text-h4 text-md-h3 text-lg-h3 mb-10">
        <span class="ubuntu underlined">Контакты</span>
      </div>

      <div class="my-4">
        <div class="contact-title">Отдел продаж</div>

        <v-row class="no-gutters mt-4">
          <v-col cols="3" class="d-flex flex-column px-4">
            <div class="contact-subtitle">Телефон</div>
            <br />
            <div class="contact-subtitle">Email</div>
            <div class="contact-subtitle">Адрес</div>
          </v-col>
          <v-col cols="8" offset="1" offset-md="0" md="6">
            <div>+7 (495) 645-18-01</div>
            <div>+7 (495) 604-16-44</div>
            <div>sales@biofarma.ru</div>
            <div>
              Москва, Хлебозаводский проезд 7 стр. 9,<br />
              Бизнес-центр Калейдоскоп
            </div>
          </v-col>
        </v-row>
      </div>
      <div class="my-4">
        <div class="contact-title">Уполномоченный по фармаконадзору</div>

        <v-row class="no-gutters mt-4">
          <v-col cols="3" class="d-flex flex-column px-4">
            <div class="contact-subtitle">Телефон</div>
            <div class="contact-subtitle">Email</div>
          </v-col>
          <v-col cols="8" offset="1" offset-md="0" md="6">
            <div>+7 (926) 515-30-87</div>
            <div>tak@biofarma.ru</div>
          </v-col>
        </v-row>
      </div>
      <div class="my-4">
        <div class="contact-title">Отдел претензий</div>

        <v-row class="no-gutters mt-4">
          <v-col cols="3" class="d-flex flex-column px-4">
            <div class="contact-subtitle">Телефон</div>
            <div class="contact-subtitle">Email</div>
          </v-col>
          <v-col cols="8" offset="1" offset-md="0" md="6">
            <div>+7 (926) 515-30-87</div>
            <div>med@biofarma.ru</div></v-col
          >
        </v-row>
      </div>
      <div class="my-4">
        <div class="contact-title">Основной склад</div>

        <v-row class="no-gutters mt-4">
          <v-col cols="3" class="d-flex flex-column px-4">
            <div class="contact-subtitle">Адрес</div>
          </v-col>
          <v-col cols="8" offset="1" offset-md="0" md="6">
            <div>
              Москва, Хлебозаводский проезд 7 стр. 9, Бизнес-центр Калейдоскоп
            </div>
          </v-col>
        </v-row>
      </div>
      <div class="my-4">
        <div class="contact-title">Дополнительный склад</div>

        <v-row class="no-gutters mt-4">
          <v-col cols="3" class="d-flex flex-column px-4">
            <div class="contact-subtitle">Адрес</div>
          </v-col>
          <v-col cols="8" offset="1" offset-md="0" md="4">
            <div>
              Московская область, Индустриальный парк Андреевское, Ленинский
              район
            </div>
          </v-col>
        </v-row>
      </div>
    </v-container>
  </v-col>
</template>
<script>
export default {
  computed: {
    contactsPosition() {
      switch (this.$vuetify.breakpoint.name) {
        case "lg":
          return {
            style: "position:absolute",
            size: "",
          };
        case "xl":
          return {
            style: "position:absolute",
            size: "",
          };
        case "md":
          return {
            style: "position:absolute",
            size: "",
          };
        default:
          return {
            style: "",
            size: "",
          };
      }
    },
  },
};
</script>

<style scoped>
.contants-wrapper {
  -webkit-box-shadow: 0px 0px 11px 0px rgba(34, 60, 80, 0.2);
  -moz-box-shadow: 0px 0px 11px 0px rgba(34, 60, 80, 0.2);
  box-shadow: 0px 0px 11px 0px rgba(34, 60, 80, 0.2);
}
.contact-title {
  font-size: 20px;
}
.contact-subtitle {
  font-weight: 400;
  font-size: 16px;
  color: rgb(120, 120, 120);
}
</style>