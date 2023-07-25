<template>
  <v-sheet>
    <v-row>
      <v-img src="../assets/img/header-text-2.png"></v-img>
    </v-row>
    <v-row class="d-flex align-start flex-column mx-12 my-8">
      <v-row v-for="(item, index) in divList" :key="index" class="d-flex my-2">
        <v-card class="card py-2 px-8 py-4">{{ item.number }}</v-card>
        <v-card class="d-flex pa-2 InputCard" width="458px" height="60px">
          <span v-if="item.stat == 'Active'" class="active d-flex py-2">
            <v-img src="../assets/img/active.png"></v-img>
          </span>
          <span v-else class="deactive d-flex py-2">
            <v-img src="../assets/img/deactive.png"></v-img>
          </span>
          <h3
            class="d-flex"
            style="font-size: 1em; margin-top: 10px"
            align="center"
          >
            {{ item.plan }}
          </h3>
          <span class="delete d-flex py-2">
            <v-img
              src="../assets/img/delete.png"
              @click="RemovePlan(index)"
            ></v-img>
          </span>
        </v-card>
      </v-row>
    </v-row>

    <v-row>
      <h3>برنامه جدید</h3>
    </v-row>
    <v-row>
      <v-col cols="4">
        <v-textarea
          v-model="plan"
          label="برنامه جدید"
          outlined
          width="100px"
          height="50px"
        ></v-textarea>
      </v-col>
      <v-col cols="3" class="add">
        <v-img src="../assets/img/add.png" @click="AddPlan"></v-img>
      </v-col>
    </v-row>
  </v-sheet>
</template>

<script>
export default {
  name: "PlanComponent",
  data: () => ({
    plan: "",
    count: 6,
    status: "Active",
    divList: [
      { number: 1, stat: "Active", plan: "برنامه اول" },
      { number: 2, stat: "Active", plan: "برنامه اول" },
      { number: 3, stat: "Active", plan: "برنامه اول" },
      { number: 4, stat: "Deactive", plan: "برنامه اول" },
      { number: 5, stat: "Deactive", plan: "برنامه اول" },
    ],
  }),
  methods: {
    AddPlan() {
      this.divList.push(this.count, this.status, this.plan);
    },
    RemovePlan(index) {
      this.divList.splice(index, 1);
    },
  },
};
</script>
<style scoped>
.card {
  background-color: rgb(12, 170, 255);
  color: #1d59b3;
  border: 3px solid #1d59b3;
}
.InputCard {
  margin-right: 1em;
}
.active {
  margin-left: 3em;
}
.deactive {
  margin-left: 2em;
}
.delete {
  margin-right: 10em;
}
.add {
  padding-left: 3em;
  padding-top: 1.5em;
}
</style>
