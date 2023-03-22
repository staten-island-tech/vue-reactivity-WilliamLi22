<!-- <NotWelcome /> -->
<template>
  <div class="home"></div>
  <li v-for="ingredients in ingredients" :key="ingredients">
    {{ ingredients }}
  </li>
  <button v-for="ingredients in ingredients" :key="ingredients"></button>
</template>

<!-- <script setup>
import NotWelcome from "../components/NotWelcome.vue";
</script> -->

<script>
export default {
  name: "home",
  components: {},
  data() {
    return {
      message: "",
      ingredients: [
        "Lettuce $1",
        "Shredded Mozzarella $2",
        "Cheddar Cheese $2",
        "Bacon $3",
        "Meatballs $3",
        "Grilled Chicken $3",
        "Ham $3",
        "Steak $4",
        "Tuna $3",
        "Cucumber $1",
        "Pickles $1",
        "Tomato $1",
      ],
    };
  },
  computed: {},
  methods: {},
};
</script>

<style scoped></style>
