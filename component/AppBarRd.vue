<template>
  <v-card>
    <v-layout>
      <v-app-bar color="#c8b6c4" proeminent>
        <v-app-bar-nav-icon
          v-if="$vuetify.display.xs"
          variant="text"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>

        <v-toolbar-title>Robson Cleiton Neto</v-toolbar-title>
      </v-app-bar>

      <v-navigation-drawer :permanent="!$vuetify.display.xs" v-model="drawer">
        <v-list :items="items"> </v-list>
      </v-navigation-drawer>

      <v-main style="height: 500px">
        <v-card-text> whathever </v-card-text>
      </v-main>
    </v-layout>
  </v-card>
</template>
    
    <script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        { title: "1", value: "abobora" },
        { title: "2", value: "quiabo" },
        { title: "3", value: "vagem" },
      ],
    };
  },
};
</script>