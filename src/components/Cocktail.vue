<template>
  <div>
    <v-row align="center" justify="center">
      <b>{{ this.cocktail.name }}</b>
    </v-row>
    <v-row align="center" justify="center">
      {{ this.cocktail.description }}
    </v-row>
    <v-row align="center" justify="center">
      <i>{{ this.ingredientsString }}</i>
    </v-row>
    <v-row class="px-12 py-2">
      <v-divider/>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Cocktail",
  props: {
    cocktail: Object,
  },
  computed: {
    ingredientsString: function () {
      return this.cocktail.ingredients.join(" | ");
    },
  },
};
</script>

<style scoped>
</style>