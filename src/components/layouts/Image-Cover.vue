<template>
    <img src="/assets/photo1.png" alt="cake" class="cover-image">
</template>

<script>
export default {
    name: 'cover'
}
</script>

<style lang="scss">
@import "../../scss/mixins";
  .cover-image {
    padding-top: 12px;
    width: 335px;
    height: 208px;

    @include breakpoint('s'){
        width: 90%;
        height: 100%;
        padding-top: 28px;
    }

    @include breakpoint('m'){
        width: 970px;
        height: 470px;
        padding-top: 44px;
    }
}
</style>