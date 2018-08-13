<template>
  <section class="single-recipe">
    <h1>TITLE {{ $route.params.id }}: {{ recipe.title }}</h1>
    <div>
      <img :src="recipe.thumbnail" alt="" />
    </div>
    <p>{{ recipe.previewText }}</p>
  </section>
</template>

<script>
  import recipes from '@/data/recipes';

  export default {
    asyncData(context) {
      // it auto-resolves axios promoses though
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({ recipe: recipes.find(el => el.id === context.params.id) })
        }, 2000);
      });
    }
  }
</script>


<style scoped>
  .single-recipe {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
    flex-flow: column;
  }
</style>
