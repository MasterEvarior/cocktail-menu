<template>
    <v-list-item>
        <v-list-item-icon link to="category.url">
            <v-icon v-text="category.icon">glass-cocktail</v-icon>
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