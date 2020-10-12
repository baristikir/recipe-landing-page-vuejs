<template>
    <div class="ingredients__section">
        <h2 class="ingredients__section-heading">Ingredients
        </h2>
        <IngredientInfoElement
        v-for="(element, index) in recipeElements"
        :key="index"
        :recipeElement="element">
        </IngredientInfoElement>
    </div>
</template>

<script>
import IngredientInfoElement from "@/components/content/Info-Ingredients.vue";
export default {
    components: {
        IngredientInfoElement,
    },
    props:{
        recipeElements: Array,
    },
};
</script>

<style lang="scss">
@import "../../scss/variables";
@import "../../scss/mixins";
@import "../../scss/globals";

.ingredients__section{
    order: 2;
    @include breakpoint(s){
        width: 60%;
        order: 0;
    }

    &-heading{
        font-family: $playfair;
        font-size: $heading-mobile;
        font-weight: $bold;
        margin: 0;
        
        @include breakpoint('s'){
            font-size: $heading-desktop;
        }
    }
}
</style>