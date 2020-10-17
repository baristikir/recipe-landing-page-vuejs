<template>
    <img src="/assets/photo1.png" alt="cake" class="cover-image">
</template>

<script>
export default {
    name: 'cover'
}
</script>

<style lang="scss">
// ************ //
// * Import's * //
// ************ //
@import "../../scss/mixins";

// ************ //
// * Stylings * //
// ************ //
.cover-image {
    padding-top: 12px;
    max-width: 100%;
    height: auto;
}
</style>