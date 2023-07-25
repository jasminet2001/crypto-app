<template>
  <v-sheet class="main">
    <v-card class="my-16" width="95%">
      <TopRowComponent />
      <PlanComponent style="width: 60%; margin-right: 17em" />
      <SidebarComponent />
      <drag-drop-component
        style="
          width: 70%;
          margin-right: 17em;
          margin-top: 1em;
          padding-bottom: 15em;
        "
      />
    </v-card>
  </v-sheet>
</template>
<script>
import TopRowComponent from "./TopRowComponent.vue";
import SidebarComponent from "./SidebarComponent.vue";
import DragDropComponent from "./DragDropComponent.vue";
import PlanComponent from "./PlanComponent.vue";
export default {
  name: "MainCardComponent",

  components: {
    SidebarComponent,
    DragDropComponent,
    PlanComponent,
    TopRowComponent,
  },

  data: () => ({
    //
  }),
};
</script>
<style scoped>
.main {
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

