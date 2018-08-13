<template>
  <section class="recipes">
    <Header />
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :id="recipe.id"
      :previewText="recipe.previewText"  />
  </section>
</template>

<script>
  import Recipe from '@/components/Recipe';
  import recipes from '@/data/recipes';

  export default {
    components: { Recipe },
    asyncData() {
      // it auto-resolves axios promoses though
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({ recipes })
        }, 2000);
      });
    }
  }
</script>


<style scoped>
  .recipes {
    color: #000;
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
  }
</style>

