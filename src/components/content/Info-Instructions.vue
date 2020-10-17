<template>
    <li class="instruction__list-element">
        <div class="">
            <div class="instruction__list-counter">{{number}}</div>
        </div>
        <span class="instruction__list-text" v-html="step"></span>
    </li>
</template>

<script>
export default {
    props: {
        step: String,
        number: Number,
    },
    computed: {
    instructionNumber () {
      return this.$vnode.key + 1;
    },
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
.instruction__list{

    &-element{
        display: flex;
        flex-direction: row;
        margin-bottom: 2.5rem;
    }

    &-counter{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        margin-right: 1rem;
        padding-bottom: .1rem;
        width: 2.25rem;
        height: 2.25rem;
        background: $orange;
        border-radius: .5rem;
        color: white;
        font-size: 1rem;
        font-weight: $bold;
        font-family: $playfair;
    }

    &-text{
        font-size: $instruction-text;
    }
}
</style>