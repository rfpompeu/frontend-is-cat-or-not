<template>
  <v-app>
    <v-app-bar app>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          :src="require('./cat_logo.png')"
          width="100"
        />
        <span class="mr-2">Is cat or not?</span>
      </div>

      <v-spacer></v-spacer>

      <v-btn href="/about" class="mx-2" fab dark small color="dark">
        <v-icon> mdi-help</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
