<template>
    <div>
        <h3 class="ingredient__heading">
        <!-- Recipe Name -->
        {{recipeElement.name}}
        </h3>    
        <!-- Recipe Ingredients Iteration Here-->
        <div v-for="(ingredient, index) in recipeElement.ingredients" :key="index">
        <label class="ingredient__info">
            <input type="checkbox" class="ingredient__info-checkbox" />
            <span class="ingredient__info-text" v-html="ingredient">
                
            </span>
        </label>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Info-Ingredients',
    props: {
        recipeElement: Object,
    },    
}
</script>

<style lang="scss">
@import "../../scss/variables";
@import "../../scss/mixins";
@import "../../scss/globals";
.ingredient__heading{
    font-family: $playfair;
    font-size: $subheading-mobile;
    font-weight: $regular;
    font-style: $italic;
    color: $gray-second;

    @include breakpoint('s'){
        font-size: $subheading-desktop;
    }
}
.ingredient__info{
    display: flex;
}
</style>