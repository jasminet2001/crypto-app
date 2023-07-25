<template>
  <v-app id="app" style="font-family: 'Yekan', sans-serif">
    <AppbarComponent />
    <HeaderComponent />
    <MainCardComponent />
  </v-app>
</template>

<script>
import MainCardComponent from "./components/MainCardComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import AppbarComponent from "./components/AppbarComponent.vue";
export default {
  name: "App",

  components: {
    MainCardComponent,
    HeaderComponent,
    AppbarComponent,
  },

  data: () => ({
    //
  }),
};
</script>
<style>
@import "assets/main.css";
#app {
  background: hsla(191, 79%, 82%, 1);
  background: linear-gradient(
    180deg,
    hsla(191, 79%, 82%, 1) 20%,
    hsla(318, 100%, 89%, 1) 100%
  );

  background: -moz-linear-gradient(
    180deg,
    hsla(191, 79%, 82%, 1) 20%,
    hsla(318, 100%, 89%, 1) 100%
  );

  background: -webkit-linear-gradient(
    180deg,
    hsla(191, 79%, 82%, 1) 20%,
    hsla(318, 100%, 89%, 1) 100%
  );

  filter: progid: DXImageTransform.Microsoft.gradient( startColorstr="#ABE7F5", endColorstr="#FFC7EE", GradientType=1 );
}
</style>

