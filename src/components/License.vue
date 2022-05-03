<template>
  <div
    class="wrapper d-flex justify-center align-center flex-column py-6 my-md-16"
  >
    <div class="underlined license-title">Лицензия</div>
    <div
      class="license px-16 py-10 rounded-lg"
      :style="
        $vuetify.breakpoint.lgAndUp
          ? 'margin-left: 100px'
          : 'display:flex;flex-direction:column; justify-content:center;align-items:center;'
      "
    >
      <img
        @click="dialog = true"
        class="license-image my-4"
        :style="
          $vuetify.breakpoint.name == 'xl'
            ? 'transform: translate(-120%, -50%);position:absolute;top:50%'
            : $vuetify.breakpoint.name == 'lg'
            ? 'transform: translate(-105%, -50%);position:absolute;top:50%'
            : 'position:relative'
        "
        height="320"
        src="../assets/license.jpg"
      />
      <span v-if="$vuetify.breakpoint.lgAndUp">
        Обладая большой компетенцией в построении фармацевтического бизнеса с
        нуля, наша компания помогает создать объекты фармацевтической отрасли ,и
        получить лицензии на оптовую фармацевтическую деятельность и перевозку
        медикаментов. Наши специалисты рады проконсультировать вас ,на любом
        этапе построения этого бизнеса :от регистрации юридического лицаи
        строительства складов,до финального получения фармацевтической лицензии
        и начала ведения бизнеса.
      </span>
    </div>
    <v-dialog
      v-model="dialog"
      :width="
        $vuetify.breakpoint.mdAndUp
          ? '500px'
          : $vuetify.breakpoint.smAndDown
          ? '80%'
          : '450px'
      "
    >
      <div>
        <v-img src="../assets/license.jpg" />
      </div>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
    };
  },
};
</script>

<style scoped>
.license {
  position: relative;
  box-shadow: 0px 0px 13px 0px rgba(34, 60, 80, 0.2);
  max-width: 1000px;
}
.license-title {
  font-weight: 700;
  font-size: 36px;
}
.dialog {
  width: 100px;
}
</style>