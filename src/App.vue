<template>
<div class="container">
  <Header 
    :title="recipe.name"
    :description="recipe.description"
  />
  <ImageCover/>
  <section>
    <Ingredients
      :recipeElements="recipe.elements">
    </Ingredients>
  </section>
  <Footer/>
</div>
</template>

<script>
import Header from './components/layouts/Header.vue'
import Footer from './components/layouts/Footer.vue'
import ImageCover from './components/layouts/Image-Cover.vue'
import Ingredients from './components/layouts/Ingredients.vue'

export default {
  name: 'App',
  components: {
    Header,
    ImageCover,
    Ingredients,
    Footer,
  },
  data(){
    return{
      recipe: {
        name: "Classic Cheesecake Recipe",
        description: "Look no further for a creamy and ultra smooth classic cheesecake recipe! Paired with a buttery graham cracker crust, no one can deny its simple decadence. For the best results, bake in a water bath.",
        elements: [
          {
            name: "Graham Cracker Crust",
            ingredients: [
              "for 8-ounce blocks (904g) full-fat <strong>cream cheese</strong>, softened to room temperature",
              "1 cup (200g) <strong>granulated sugar</strong>",
              "1 cup (240g) full-fat <strong>sour cream</strong>, at room temperature",
              "1 teaspoon <strong>pure vanilla extract</strong>",
              "2 teaspoons <strong>fresh lemon juice</strong> (optional, but recommended)",
              "3 large <strong>eggs</strong>, at room temperature",
              "topping suggestions: <i>salted caramel, lemmon curd, strawberry topping, chocolate ganache, red wine chocolate ganache, fresh fruit, whupped cream, or raspberry sauce (recipe in notes)</i>",
            ],
          },
        ],

      }
    }
  }
};
</script>

<style lang="scss">

</style>
