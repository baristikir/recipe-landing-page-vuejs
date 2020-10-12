<template>
    <div class="info__section">
        <div class="card__info">
            <InfoCard
             v-for="(element,index) in recipeInfo"
             :key="index"
             :element="element"
             ></InfoCard>
        </div>
    </div>
</template>

<script>
import InfoCard from '../content/Info-Card.vue';
export default {
    name: 'card',
    components: {
        InfoCard,
    },
    props: {
        recipeInfo: Array,
    },
};
</script>

<style lang="scss">
@import "../../scss/variables";
@import "../../scss/mixins";
@import "../../scss/globals";

.info__section{
    display: flex;
    flex-direction: column;

    @include breakpoint(s){
        width: 40%;
    }
}

.card__info{
    display: flex;
    flex-wrap: wrap;
    align-self: flex-end;
    flex-direction: row;
    padding-bottom: 1rem;
    border-radius: 0.5rem;

    @include breakpoint(s){
        width: auto;
        flex-direction: column;
        padding-left: 2.5rem;
        padding-right: 4rem;
        padding-top: 2.5rem;
        box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.12);
    }

}
</style>