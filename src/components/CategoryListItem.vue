<template>
    <v-list-item link :to="category.url">
        <v-list-item-icon>
            <v-icon>{{category.icon}}</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
            <v-list-item-title v-text="category.name"></v-list-item-title>
        </v-list-item-content>
    </v-list-item>
</template>

<script>
export default {
    name: 'CategoryListItem',
    props:{
        category: Object
    }
}
</script>