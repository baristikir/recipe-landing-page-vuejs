<template>
<div class="container">
  <Header 
    :title="recipe.name"
    :description="recipe.description"
  />
  <ImageCover/>
  <section class="flex content-section">
    <Ingredients
      :recipeElements="recipe.elements">
    </Ingredients>
    <Card
     :recipeInfo="recipe.infos">
     </Card>
  </section>
  <div>
    <Instructions 
     :recipeInstructions="recipe.instructions"></Instructions>
  </div>
  <Footer/>
</div>
</template>

<script>
import Header from './components/layouts/Header.vue'
import Footer from './components/layouts/Footer.vue'
import ImageCover from './components/layouts/Image-Cover.vue'
import Ingredients from './components/layouts/Ingredients.vue'
import Card from './components/layouts/Card.vue'
import Instructions from './components/layouts/Instructions.vue'

export default {
  name: 'App',
  components: {
    Header,
    ImageCover,
    Ingredients,
    Card,
    Instructions,
    Footer,
  },
  data: function() {
    return {
      recipe: {
        name: "Classic Cheesecake Recipe",
        description: "Look no further for a creamy and ultra smooth classic cheesecake recipe! Paired with a buttery graham cracker crust, no one can deny its simple decadence. For the best results, bake in a water bath.",
        elements: [
          {
            name: "Cheesecake",
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
          {
            name: "Graham Cracker Crust",
            ingredients: [
              "1 and 1/2 cups (150g) <strong>graham cracker crumbs</strong> (about 10 full sheet graham crackers)",
              "5 Tablespoons (70g) <strong>unsalted butter</strong>, melted",
              "1/4 cup (50g) <strong>granulated sugar</strong>",
            ],
          }
        ],
        infos: [
          {
            heading: "Yields",
            data: "12 servings",
            icon: "local_dining",
            color: "icon-orange",
          },
          {
            heading: "Prep time",
            data: "45 minutes",
            icon: "schedule",
            color: "icon-black",
          },
          {
            heading: "Cook time",
            data: "1 hour",
            icon: "schedule",
            color: "icon-black",
          },
          {
            heading: "Total time",
            data: "7,75 hours",
            icon: "schedule",
            color: "icon-black",
          },
        ],
        instructions: [
          "Adjust the oven rack to the lower-middle position and preheat oven to 150ºF (177ºC)",
          "<strong>Make the crust:</strong> Using a good processor, pulse the graham crackers into crumbs. Pour into a medium bowl and stir in sugar and melted butter until combined. (You can algo pulse it all together in the food processor). Mixture will be sandy. Press firmly into the bottom and slightly up the sides of a 9-inch or 10-inch springform pan. No need to grease the pan first. I use the bottom of measuring cup to pack the crust down tightly. Pre-bake for 8 minutes. Remove from the oven and place the hot pan on a large piece of aluminium foil. The foil will wrap around the pan for the water batch in step 4. Allow crust to slightly cool as you prepare the filling.",
          "<strong>Make the filling:</strong> Using a handheld or stand mixer fitted with a paddle attachment, beat the cream cheese and granulated sugar together on medium-high speed in a large bowl until the mixture is smooth and creamy, about 2 minutes. Add the sour cream, vanilla extract, and lemon juice then beat until fully combined. On medium speed, add the eggs one at a time, beating after each addition until just blended. After the final egg is incorporated into the batter, stop mixing. To help prevent the cheesecake from deflating and cracking as it cools, avoid over-mixing the batter as best you can",
          "<strong>Prepare the simple water bath (see note)</strong> Boil a pot of water. You need 1 inch of water in your roasting pan for the water bath, so make sure you boil enough. I use an entire kettle of hot water. As the water is heating up, wrap the aluminum foil around the springform pan. Pour the cheesecake batter on top of the crust. Use a rubber spatula or spoon to smooth it into an even layer. Place the pan inside of a large roasting pan. Carefully pour the hot water inside of the pan and place in the oven. (Or you can place the roasting pan in the oven first, then pour the hot water in. Whichever is easier for you.)",
          "Bake cheesecake for 55-70 minutes or until the center is almost set. When it’s done, the center of the cheesecake will slightly wobble if you gently shake the pan. Turn the oven off and open the oven door slightly. Let the cheesecake sit in the oven in the water bath as it cools down for 1 hour. Remove from the oven and water bath, then cool cheesecake completely at room temperature. Then refrigerate the cheesecake for at least 4 hours or overnight.",
          "Use a knife to loosen the chilled cheesecake from the rim of the springform pan, then remove the rim. Using a clean sharp knife, cut into slices for serving. For neat slices, wipe the knife clean and dip into warm water between each slice.",
          "Serve cheesecake with desired toppings. Cover and store leftover cheesecake in the refrigerator for up to 5 days.",
        ],
      },
    };
  },
};
</script>

<style lang="scss">
@import "./scss/variables";
@import "./scss/mixins";
@import "./scss/globals";
.content-section{
  flex-direction: column;
  margin-top: 2rem;
  margin-bottom: 2rem;

  @include breakpoint(s){
    flex-direction: row;
  }
}
</style>
