<template>
  <v-app>
    <v-app-bar app dark clipped-right>
      <v-spacer />
      🍹Cocktail Menu🍹
      <v-spacer />
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    </v-app-bar>

    <v-navigation-drawer clipped app dark right v-model="drawer">
      <v-list>
        <CategoryListItem
          v-for="category in categories"
          v-bind:key="category.name"
          :category="category"
        />
      </v-list>
    </v-navigation-drawer>
    <v-main> 
      <router-view/>
    </v-main>
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
      categories: categories,
    };
  },
};
</script>
