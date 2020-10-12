<template>
    <div class="card"
     :class="element.heading === 'Yields' ? 'row-full-width single-row' : 'partial-width'">
        <i class="material-icons card__info-icon" 
         :class="element.color">
            {{element.icon}}
        </i>
        <div class="card__text">
            <span class="card__subtitle uppercase">
                {{element.heading}}
            </span>
            <span class="card__info-text">
                {{element.data}}
            </span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Info-Card',
    props: {
        element: Object,
    },
};
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
// * Styling for Material Icon * // 
.card__info-icon{
    margin-right: 1rem;
    font-size: 1.125rem;
    @include breakpoint(s){
        font-size: 1.875rem;
    }
}

// * Card Styling with Flexbox * //
.card{
    display: flex;
    flex-shrink: 0;
    align-items: center;
    flex-direction: row;
    margin-bottom: 2rem;
    order: 9999;
    margin-bottom: 2rem;
    width: 33%;

    // * Min-Width 667px * //
    @include breakpoint(s){
        width: auto;
    }

    // * Container for Text's * //
    &__text{
        display: flex;
        flex-direction: column;
        width: auto;
    }

    // * Subtitle for Info Property* //
    &__subtitle{
        color: $gray-second;
        font-size: $info-subtitle-mob;
        font-weight: $bold;

        @include breakpoint(s){
            font-size: $info-subtitle-desk;
        }
    }

    // * Info Text inside Card under Subtitle's * //
    &__info-text{
        font-size: $info-mobile;

        @include breakpoint(s){
            font-size: $info-desktop;
        }
    }
}


// ****************** //
// * Helper Classes * //
// ****************** //

// * Icon Color: Color * //
.icon-orange{
    color: $orange;
}

// * Icon Color: Black * //
.icon-black{
    color: black;
}

// * Full Width Changer Class * //
.row-full-width{
    width: 100%;
}

// * 1/3 Partial Width Changer Class * //
.partial-width{
    width: 33.3%;

    @include breakpoint(s){
        width: auto;
    }
}

// * For Mobile first Info Element Full Width Class * //
.single-row{
    flex-shrink: 0;
}

// * Text Transformations * //
.uppercase{
    text-transform: uppercase;
}
</style>