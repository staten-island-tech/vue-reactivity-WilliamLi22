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
        {
          name: "Lettuce",
          type: "vegetable",
          image: "https://assets.bonappetit.com/photos/57e1807fbf7e91497a10e216/16:9/w_1280,c_limit/lettuce-640.jpg",
          price: 1
        },
        {
          name: "Cucumber",
          type: "vegetable",
          image: "https://t3.ftcdn.net/jpg/03/24/22/42360_F_324224284_KEgkz9bGAROme3X5j9k3ddwiHm3BE2IO.jpg",
          price: 1
        },
        {
          name: "Tomato",
          type: "vegetable",
          image: "https://s3.envato.com/files/3254570842019_09_Victor_food_IMG_0072-2-Edit_20190513.jpg",
          price: 1
        },
        {

        }
        "Shredded Mozzarella $2",
        "Cheddar Cheese $2",
        "Bacon $3",
        "Meatballs $3",
        "Grilled Chicken $3",
        "Ham $3",
        "Steak $4",
        "Tuna $3",
        "Pickles $1",
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
