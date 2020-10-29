<template>
  <v-app>
    <v-app-bar flat app dark clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-spacer />
      <v-btn text @click="$vuetify.theme.dark = !$vuetify.theme.dark">
        <v-icon v-if="$vuetify.theme.dark"> mdi-weather-sunny </v-icon>
        <v-icon v-else> mdi-weather-night </v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer clipped app dark left v-model="drawer">
      <v-list>
        <CategoryListItem
          v-for="category in categories"
          v-bind:key="category.name"
          :category="category"
        />
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import { categories } from "./assets/cocktails.json";
import CategoryListItem from "./components/CategoryListItem";

export default {
  name: "App",
  components: {
    CategoryListItem,
  },
  data() {
    return {
      drawer: false,
      categories: categories,
    };
  },
};
</script>
