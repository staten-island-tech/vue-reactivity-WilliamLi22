<!-- <NotWelcome /> -->
<template>
  <div class="home" v-for="ingredients in ingredients">
    <li :key="ingredients">
      {{ ingredients }}
    </li>
    <Button @click="authState" :key="ingredients">Add to Sandwich</Button>
  </div>
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
  methods: {
    authState: function name() {
      console.log("E");
    },
  },
};
</script>

<style scoped></style>
