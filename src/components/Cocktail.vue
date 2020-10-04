<template>
  <div>
    <v-row align="center" justify="center">
      <b>{{ this.cocktail.name }}</b>
    </v-row>
    <v-row align="center" justify="center" class="px-12">
      {{ this.cocktail.description }}
    </v-row>
    <v-row align="center" justify="center" class="px-12">
      <i>{{ this.ingredientsString }}</i>
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