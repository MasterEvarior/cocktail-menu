<template>
  <v-card dark min-height="100%" class="pb-1">
    <v-card-title>
      <span class="title font-weight-bold">{{ this.cocktail.name }}</span>
      <v-spacer/>
      <v-chip-group>
        <Label v-if="this.cocktail.requestOnly" tooltip='Only on request' icon='mdi-mail'/>
      </v-chip-group>
    </v-card-title>
    <v-card-text class="headline">
      <span class="description">{{ this.cocktail.description }}</span> <br>
      <span>{{ this.ingredientsString }}</span>
    </v-card-text>
  </v-card>
</template>

<script>
import Label from './Label';

export default {
  name: "Cocktail",
  components: {
    Label
  },
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