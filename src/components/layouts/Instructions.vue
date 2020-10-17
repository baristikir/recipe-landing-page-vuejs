<template>
    <div class="instructions-partial-width">
        <h2 class="instructions__section-heading">
            Instructions
        </h2>
        <ol class="instructions">
            <InstructionsInfoElement
             v-for="(step, index) in recipeInstructions"
            :key="index"
            :step="step.text"
            :number="index+1"
        ></InstructionsInfoElement>
        </ol>
    </div>
</template>


<script>
import InstructionsInfoElement from "@/components/content/Info-Instructions.vue";
export default {
    components: {
        InstructionsInfoElement,
    },
    props: {
        recipeInstructions: Array,
    },
}
</script>

<style lang="scss">
// ************ //
// * Import's * //
// ************ //
@import "../../scss/variables";
@import "../../scss/mixins";
@import "../../scss/globals";

// ************ //
// * Stylings * //
// ************ //
.instructions{
    margin: 0;
    padding: 0;
    padding-top: 2rem;
}
.instructions__section-heading{
    font-family: $playfair;
    font-size: $instruction-heading;
    font-weight: $bold;
    margin: 0;
}

// ****************** //
// * Helper Classes * //
// ****************** //
.instructions-partial-width{
   @include breakpoint(s){
        width: 60%;
    }
}
</style>