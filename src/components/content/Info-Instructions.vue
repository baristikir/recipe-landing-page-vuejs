<template>
    <li class="instruction__list-element">
        <div class="">
            <div class="instruction__list-counter"></div>
        </div>
        <span class="instruction__list-text" v-html="step"></span>
    </li>
</template>

<script>
export default {
    props: {
        step: String,
    },
};
</script>

<style lang="scss">
@import "../../scss/variables";
@import "../../scss/mixins";
@import "../../scss/globals";

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
        font-size: 1rem;
        width: 3rem;
        height: 3rem;
        background: $orange;
        border-radius: .5rem;
    }

    &-text{

    }
}
</style>