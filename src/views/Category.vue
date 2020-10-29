<template>
  <v-container class="category">
    <h1>{{category.name}}</h1>
    <span>{{category.description}}</span>
    <v-layout row wrap justify-center>
      <v-flex class="ma-2" xs12 sm6 md6 lg4 xl3 v-for="cocktail in category.cocktails" :key="cocktail.name">
          <Cocktail :cocktail="cocktail"/>
      </v-flex>
    </v-layout>
    <v-row v-for="subCategory in category.subCategories" :key="subCategory.key">
      <SubCategory :subCategory="subCategory"/>
    </v-row> 
  </v-container>
</template>

<script>
import { categories } from "../assets/cocktails.json";
import Cocktail from "../components/Cocktail";
import SubCategory from "../components/SubCategory";

export default {
  name: "Category",
  components: {
    SubCategory,
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