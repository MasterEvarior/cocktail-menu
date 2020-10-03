<template>
    <div>
        {{this.cocktail}}
        {{this.ingredientsString}}
    </div>
</template>

<script>
export default {
    name: 'Cocktail',
    props:{
        cocktail: Object
    },
    computed: {
        ingredientsString: function() {
            return "lo";
        }
    }
}
</script>