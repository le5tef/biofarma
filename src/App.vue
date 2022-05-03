<template>
  <v-app id="app" style="min-height: 100vh">
    <v-main class="d-flex flex-column">
      <SubHeader />
      <div class="fill-height" style="flex: 1">
        <router-view />
      </div>
    </v-main>
  </v-app>
</template>

<script>
import SubHeader from "./components/SubHeader.vue";
import "animate.css";
export default {
  components: {
    // Footer,
    // Header,
    SubHeader,
    // PreLoader,
  },
  methods: {
    hidePreloader: function () {
      var preloader = document.getElementById("preloader");
      preloader.style.display = "none";
    },
  },

  created() {
    // window.addEventListener("load", this.hidePreloader);
    window.onload = () => {
      this.hidePreloader();
    };
  },
};
</script>

<style>
#app {
  /* background: url("./assets/gradientlogo1.png"); */

  background-repeat: no-repeat;
}
.v-main__wrap {
  display: flex;
  flex-direction: column;
}
.croogla {
  font-family: "Croogla";
  font-weight: 100;
  font-size: 18px;
}
.oswald {
  font-family: "Oswald";
}
.ubuntu {
  font-family: "Ubuntu";
}
.russo {
  font-family: "Russo";
}
.outlined {
  -webkit-box-shadow: 8px 9px 0px -1px rgb(50 186 71);
  -moz-box-shadow: 8px 9px 0px -1px rgb(50 186 71);
  box-shadow: 8px 9px 0px -1px rgb(50 186 71);
}
.underlined {
  -webkit-box-shadow: 0px 5px 0px -1px rgb(50 186 71);
  -moz-box-shadow: 0px 5px 0px -1px rgb(50 186 71);
  box-shadow: 0px 5px 0px -1px rgb(50 186 71);
}
.card {
  background-color: white;
}
@font-face {
  font-family: "Russo";
  src: url("./assets/fonts/RussoOne.ttf");
}
@font-face {
  font-family: "Croogla";
  src: url("./assets/fonts/Croogla4F.ttf");
}
@font-face {
  font-family: "Ubuntu";
  src: url("./assets/fonts/Ubuntu-Bold.ttf");
}
@font-face {
  font-family: "Oswald";
  src: url("./assets/fonts/Oswald.ttf");
}
</style>
