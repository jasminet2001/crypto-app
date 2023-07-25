<template>
  <v-card class="overflow-hidden" dir="rtl">
    <v-navigation-drawer
      permanent
      v-model="$data[$vuetify.breakpoint.smAndDown ? 'drawer' : 'value']"
      :value="true"
      fixed
      hide-overlay
      rail
      right
      dir="rtl"
    >
      <v-list dense nav>
        <v-list-item-group active-class="grey lighten-4--text text--accent-4">
          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-dashboard-layout-100.png"
              ></v-img>
              <v-list-item-title>داشبورد</v-list-item-title>
            </v-list-item-icon>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-strategy-news-100.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>برنامه</v-list-item-title>
          </v-list-item>

          <v-list-item
            class="py-2"
            style="background-color: #2c5eff; color: white"
          >
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-rating-100.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>بسته‌های منتخب</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-alarm-100.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>هشدارها</v-list-item-title>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-pass-fail-100.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>تست نرم‌افزار</v-list-item-title>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-strategy.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>اتصالات کاربری</v-list-item-title>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-pass-fail-100.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>برنامه‌ریزی</v-list-item-title>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/Robo.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>برنامه‌ریزی هوشمند</v-list-item-title>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-customer-100 (2).png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>مشاهده پروفایل</v-list-item-title>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-online-support-100.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>پشتیبانی</v-list-item-title>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-help-100.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>راهنما</v-list-item-title>
          </v-list-item>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/no data 2.png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title>درباره ما</v-list-item-title>
          </v-list-item>

          <v-divider></v-divider>

          <v-list-item class="py-2">
            <v-list-item-icon>
              <v-img
                width="25px"
                height="25px"
                class="ml-8"
                src="../assets/img/icons8-shutdown-100 (3).png"
              ></v-img>
            </v-list-item-icon>
            <v-list-item-title class="pa-2">خروج</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>
  
  <script>
export default {
  name: "SidebarComponent",
};
</script>