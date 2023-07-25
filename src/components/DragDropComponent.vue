<template>
  <v-sheet>
    <v-row>
      <v-img src="../assets/img/header-text-1.png"></v-img>
    </v-row>
    <v-row class="d-flex my-8">
      <img
        src="../assets/img/icons8-box-important-100.png"
        height="29px"
        width="32px"
        class="mr-8 ml-2"
      />
      <h3>درصورتیکه فرمول‌نویسی باید انجام شود</h3>
    </v-row>

    <v-card color="#F4F7FB" class="py-8">
      <v-row>
        <v-col cols="2">
          <h3 class="first">برنامه</h3>
        </v-col>
        <v-col cols="10">
          <v-card class="card d-flex justify-start align-center">
            <div>
              <draggable
                v-model="cards"
                group="cards"
                tag="v-card"
                class="d-flex"
                @change="log"
                :animation="300"
              >
                <v-card
                  v-for="(num, index) in numbers"
                  :key="index"
                  class="my-8 mx-4 px-8 py-4 item"
                  ghost-class="ghost"
                  >{{ num }}</v-card
                >
              </draggable>
            </div>
          </v-card>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="2">
          <h3 class="second">نمادها</h3>
        </v-col>
        <v-col>
          <v-card class="card d-flex justify-start" style="width: 70%">
            <div>
              <draggable
                v-model="cards"
                group="cards"
                tag="v-card"
                class="d-flex pa-4"
                @change="log"
                :animation="300"
              >
                <v-card
                  v-for="(op, index) in ops"
                  :key="index"
                  class="my-8 mx-4 px-8 py-4 op"
                  :style="{
                    backgroundColor: calculateBackgroundColor(index),
                    borderColor: calculateBorderColor(index),
                    color: calculateColor(index),
                  }"
                  >{{ op }}</v-card
                >
              </draggable>
            </div>
          </v-card>
        </v-col>
      </v-row>

      <v-row>
        <v-card class="pa-8 ma-8 formulacard" style="width: 70%">
          <div>
            <h3>لطفا فرمول را به صورت کشیدن و انداختن بنویسید.</h3>
            <draggable
              v-model="formula"
              group="cards"
              tag="v-card"
              class="d-flex pa-4"
              @change="log"
              @update="onUpdate"
              :animation="100"
            >
              <v-card
                v-for="(item, index) in formula"
                :key="index"
                class="my-8 mx-4 px-8 py-4"
                ghost-class="ghost"
                >{{ item }}</v-card
              >
            </draggable>
          </div>
        </v-card>
      </v-row>

      <v-row class="d-flex">
        <img
          src="../assets/img/fx.png"
          height="29px"
          width="32px"
          class="mr-8"
        />
        <img
          src="../assets/img/icons8-equal-sign-100.png"
          height="19px"
          width="21px"
          class="mt-2"
        />
      </v-row>
    </v-card>
  </v-sheet>
</template>

<script>
import draggable from "vuedraggable";
export default {
  name: "DragDropComponent",
  components: { draggable },
  data: () => ({
    formula: null,
    numbers: [5, 6, 7, 8, 9],
    ops: {
      add: "+",
      sub: "-",
      open: "(",
      close: ")",
    },
  }),
  methods: {
    // add: function () {
    //   // this.list.push({ name: "Juan" });
    //   console.log(elem)
    // },
    // replace: function () {
    //   this.list = [{ name: "Edgard" }];
    // },
    // clone: function (el) {
    //   return {
    //     name: el.name + " cloned",
    //   };
    // },
    log: function (evt) {
      window.console.log(evt);
    },
    onUpdate: function (evt) {
      console.log(evt);
      console.log(this.formula);
    },
    calculateBackgroundColor(index) {
      if (index == "add") {
        return "#90EE90";
      } else if (index == "sub") {
        return "pink";
      } else {
        return "orange";
      }
    },
    calculateBorderColor(index) {
      if (index == "add") {
        return "#138C08";
      } else if (index == "sub") {
        return "#B12FA5";
      } else {
        return "#AA5C00";
      }
    },
    calculateColor(index) {
      if (index == "add") {
        return "#138C08";
      } else if (index == "sub") {
        return "#B12FA5";
      } else {
        return "#AA5C00";
      }
    },
  },
};
</script>

<style scoped>
.card {
  background: var(--header-color-gray-02, #ededed);
  box-shadow: 2px 2px 10px 0px rgba(0, 0, 0, 0.15) inset;
  height: 8em;
  width: 40em;
}
.formulacard {
  background: var(--header-color-gray-02, #ededed);
  box-shadow: 2px 2px 10px 0px rgba(0, 0, 0, 0.15) inset;
  height: 15em;
  width: 40em;
}
:hover.item {
  transform: rotate(5deg);
  cursor: pointer;
}
:hover.op {
  transform: rotate(5deg);
  cursor: pointer;
}
.item {
  background-color: rgb(12, 170, 255);
  color: #1d59b3;
  border: 3px solid #1d59b3;
}
.op {
  border: 3px solid #1d59b3;
}
.first {
  padding-bottom: 5em;
  margin-right: 5em;
  margin-top: 3em;
}
.second {
  padding-bottom: 5em;
  margin-right: 5em;
  margin-top: 4em;
}
h3 {
  font-size: 15px;
}
</style>