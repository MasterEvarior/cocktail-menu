<template>
  <v-container class="category">
    <v-row align="center" justify="center">
      <h1>{{category.name}}</h1>
    </v-row>
    <v-row align="center" justify="center">
      <span>{{category.description}}</span>
    </v-row>
    <v-row class="px-4 py-2">
      <v-divider></v-divider>
    </v-row>
    <row v-for="cocktail in category.cocktails" :key="cocktail.name">
      <Cocktail :cocktail="cocktail"/>
    </row>
    <!-- <row v-for="subCategory in category.sub-categories" :key="subCategory.name">
      <SubCategory/>
    </row> -->
  </v-container>
</template>

<script>
import { categories } from "../assets/cocktails.json";
import Cocktail from "../components/Cocktail";
// import SubCategory from "../components/SubCategory";

export default {
  name: "Category",
  components: {
    // SubCategory,
    Cocktail,
  },
  computed: {
    category: function () {
      for (var i in categories) {
        if (categories[i].url === this.$route.params.category) {
          return categories[i];
        }
      }
      return {};
    },
  },
};
</script>

<style scoped>
.category {
  text-align: center;
}
</style>