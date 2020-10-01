<template>
  <header class="header">
    <div class="header__content">
      <h1 class="header__title">
        {{title}}
      </h1>
      <div class="flex header__info">
        <img style="display: flex;" src="/assets/6dots.svg" alt="dots">
        <p class="header__description">
          {{description}}
        </p>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    title: String,
    description: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "../../scss/variables";
@import "../../scss/layouts/header";
</style>
