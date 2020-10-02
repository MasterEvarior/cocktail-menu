<template>
  <v-app>
    <v-app-bar app dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-spacer />
      🍹Cocktail Menu🍹
      <v-spacer />
    </v-app-bar>

    <v-navigation-drawer app dark v-model="drawer">
      <v-list> 
        <CategoryListItem v-for="category in categories" v-bind:key="category.name" :category="category"/>
      </v-list>
    </v-navigation-drawer>

    <v-main> </v-main>
  </v-app>
</template>

<script>
import { categories } from "./assets/categories.json";
import CategoryListItem from "./components/CategoryListItem";

export default {
  name: "App",
  components: {
    CategoryListItem,
  },
  data() {
    return {
      drawer: false,
      categories: categories
    };
  },
};
</script>
