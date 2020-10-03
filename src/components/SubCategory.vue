<template>
  <div>
    <v-row>
      {{ subCategoryName }}
    </v-row>
    <v-row>
      <v-divider />
    </v-row>
  </div>
</template>


<script>
export default {
  name: "SubCategory",
  props: {
    subCategory: Object,
  },
  computed: {
    subCategoryName: function () {
      return Object.keys(this.subCategory)[0];
    },
  },
};
</script>