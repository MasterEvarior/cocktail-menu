<template>
  <div>
    <v-row>
      {{ subCategoryName }}
    </v-row>
    <v-row>
      <v-divider />
    </v-row>
    <v-row v-for="cocktail in subCategory" :key="cocktail.name">
      <Cocktail :cocktail="cocktail" />
    </v-row>
  </div>
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