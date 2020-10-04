<template>
  <v-container>
    <v-row align="center" justify="center">
      <h2>{{ this.subCategory.name }}</h2>
    </v-row>
    <v-row class="px-10 py-2">
      <v-divider/>
    </v-row>
    <v-row v-for="cocktail in subCategory.cocktails" :key="cocktail.name" align="center" justify="center">
      <Cocktail :cocktail="cocktail"/>
    </v-row>
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