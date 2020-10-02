<template>
  <div></div>
</template>

<script>
import { cocktails } from "../assets/cocktails.json";

export default {
  name: "Category",
  data() {
    return {
        cocktails: cocktails
    };
  }
};
</script>