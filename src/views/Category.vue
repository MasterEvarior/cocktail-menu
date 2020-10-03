<template>
  <v-container class="category">
    <SubCategory v-for="subCategory in this.subCategories" :key="subCategory.key" v-bind:subCategory='subCategory'/>
  </v-container>
</template>

<script>
import { categories } from "../assets/cocktails.json";
import SubCategory from "../components/SubCategory";

export default {
  name: "Category",
  components: {
    SubCategory
  },
  computed: {
    subCategories:  function(){
      return categories[this.$route.params.category];
    }
  }
};
</script>

<style scoped>
.category {
  text-align: center;
}
</style>