<template>
  <div>
    <v-row>
      {{ this.cocktail.name }}
    </v-row>
    <v-row>
      {{ this.cocktail.description }}
    </v-row>
    <v-row>
      {{ this.ingredientsString }}
    </v-row>
    <v-row>
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