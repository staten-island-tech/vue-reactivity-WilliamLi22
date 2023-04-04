<template>
  <div class="about">
    <h1>Ingredients in your sandwich:</h1>
    <div v-for="ingredient in selected" :key="ingredient.name">
      <h3>{{ ingredient.name }}</h3>
      <p>Type: {{ ingredient.type }}</p>
      <img
        :src="ingredient.image"
        :alt="ingredient.name"
        width="210"
        height="200"
      />
      <p>Price: ${{ ingredient.price }}</p>
      <Button @click="order" :key="ingredients">Remove From Sandwich</Button>
    </div>
  </div>
</template>

<script>
import {  }
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    /*     align-items: center; */
  }
}
</style>
