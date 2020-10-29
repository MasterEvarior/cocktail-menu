<template>
  <v-container>
    <h2>{{ this.subCategory.name }}</h2>
    <v-divider />
    <v-layout row wrap justify-center>
      <v-flex class="ma-2" xs12 sm6 md6 lg4 xl3 v-for="cocktail in subCategory.cocktails" :key="cocktail.name">
        <Cocktail :cocktail="cocktail" />
      </v-flex>
    </v-layout>
  </v-container>
</template>


<script>
import Cocktail from "../components/Cocktail";

export default {
  name: "SubCategory",
  components: {
    Cocktail,
  },
  props: {
    subCategory: Object,
  },
};
</script>