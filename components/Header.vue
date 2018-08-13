<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/">Starting Page</nuxt-link></li>
        <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
        <li><nuxt-link to="/about">About</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
  header {
    height: 30px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #521751;
    color: #FFF;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  li {
    margin: 0 10px;
  }

  a {
    text-decoration: none;
    color: inherit;
  }
</style>

