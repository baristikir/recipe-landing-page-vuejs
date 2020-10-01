<template>
<div class="container">
  <Header 
    title="Classic Cheesecake Recipe"
    description="Look no further for a creamy and ultra smooth classic cheesecake recipe! Paired with a buttery graham cracker crust, no one can deny its simple decadence. For the best results, bake in a water bath."
  />
  <ImageCover/>
  <Footer/>
</div>
</template>

<script>
import Header from './components/layouts/Header.vue'
import Footer from './components/layouts/Footer.vue'
import ImageCover from './components/layouts/Image-Cover.vue'

export default {
  name: 'App',
  components: {
    Header,
    ImageCover,
    Footer
  }
}
</script>

<style lang="scss">

</style>
