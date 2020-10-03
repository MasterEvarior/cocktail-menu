<template>
  <v-container class="category">
    <row v-for="cocktail in category.cocktails" :key="cocktail.name">
      <Cocktail :cocktail="cocktail"/>
    </row>
    <row>
      <SubCategory />
    </row>
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