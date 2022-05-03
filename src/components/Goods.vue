<template>
  <div
    class="wrapper d-flex text-center flex-column justify-center align-center"
  >
    <div class="goods-title mt-5">Наша продукция</div>
    <div
      :class="$vuetify.breakpoint.mdAndUp ? 'justify-center' : 'flex-column'"
      class="goods d-flex my-4 my-md-0"
    >
      <div
        class="goods--card my-md-10"
        v-for="(card, i) in goods"
        :key="i"
        @mouseover="HoverAnimation(i + 1, true)"
        @mouseleave="HoverAnimation(i + 1, false)"
      >
        <img
          width="150"
          height="150"
          :id="i + 1"
          class="animate__pulse animate__infinite pa-8 rounded-lg card-icon"
          :src="card.icon"
        />
        <div class="pt-1 pt-md-3 card-description">{{ card.data }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      goods: [
        {
          data: "Препараты крови",
          icon: require("../assets/blood.svg"),
        },
        {
          data: "Анестезиология",
          icon: require("../assets/syring.svg"),
        },
        {
          data: "Лечебное питание",
          icon: require("../assets/food.svg"),
        },
        {
          data: "Антибиотики",
          icon: require("../assets/pills.svg"),
        },
      ],
    };
  },
  methods: {
    HoverAnimation(i, val) {
      console.log(i);
      if (val) {
        document.getElementById(i).classList.add("animate__animated");
      } else {
        document.getElementById(i).classList.remove("animate__animated");
      }
    },
  },
};
</script>

<style lang='scss' scoped>
.wrapper {
  width: 100%;
}
.card-icon {
  box-shadow: 0px 0px 13px 0px rgba(17, 69, 18, 0.2);
  filter: invert(32%) sepia(54%) saturate(1012%) hue-rotate(77deg)
    brightness(99%) contrast(91%);
}
.card-description {
  font-size: 18px;
  font-family: system-ui;
  font-weight: 600;
}
.goods-title {
  font-size: 40px;
  font-weight: 700;
  width: fit-content;
}
.goods {
  gap: 40px;

  &--card {
    width: 200px;
    background-color: white;
  }
}
.benefits-title {
  font-size: 26px;
}
@media (max-width: 960px) {
  .benefits {
    gap: 20px;
  }
  .card-description {
    font-size: 13px;
  }
  .goods-title {
    margin-top: 20px;
    font-size: 30px;
    font-weight: 700;
    width: fit-content;
  }
}
</style>