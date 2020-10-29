<template>
  <v-card dark min-height="100%" class="pb-1">
    <v-card-title>
      <span class="title font-weight-bold">{{ this.cocktail.name }}</span>
    </v-card-title>

    <v-card-text class="headline">
      <span class="description">{{ this.cocktail.description }}</span> <br>
      <span>{{ this.ingredientsString }}</span>
    </v-card-text>

  </v-card>
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
.description{
  font-weight: bold;
}
</style>