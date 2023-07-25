<template>
  <v-row id="appbar" class="d-flex">
    <v-col cols="2">
      <v-btn elevation="4" rounded width="120px">1 پیغام</v-btn>
    </v-col>
    <v-col cols="2">
      <v-btn elevation="4" rounded width="120px" class="account"
        >سارا محمدیان</v-btn
      >
    </v-col>
    <v-col cols="8" class="d-flex">
      <h2 class="company">Company Name</h2>
      <v-img
        src="../assets/img/Robo.png"
        height="50px"
        width="50px"
        class="mx-16"
      ></v-img>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "AppbarComponent",
};
</script>
<style scoped>
#appbar {
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

  margin-top: 1em;
  margin-right: 20em;
}
.company {
  margin-right: 55%;
}
v-btn {
  color: #232323;
}
.account {
  border: 2px solid #41c2f9;
}
</style>
