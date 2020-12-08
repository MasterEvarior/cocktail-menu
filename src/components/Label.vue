<template>
    <v-tooltip top>
      <template v-slot:activator="{ on, attrs }">
          <v-chip 
            v-bind="attrs"
            v-on="on">
            <v-icon> {{ icon }} </v-icon>
          </v-chip>
      </template>
      <span>{{ tooltip }}</span>
    </v-tooltip>
</template>

<script>
export default {
    name: 'Label',
    props: {
        tooltip: String,
        icon: String
    }
}
</script>