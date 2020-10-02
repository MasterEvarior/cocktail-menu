<template>
  <v-app>
    <v-app-bar app dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"/>
      <v-spacer/>
      🍹Cocktail Menu🍹
      <v-spacer/>
    </v-app-bar>

    <v-navigation-drawer app dark v-model="drawer">

    </v-navigation-drawer>

    <v-main>

    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      drawer: false
    }
  }
};
</script>
