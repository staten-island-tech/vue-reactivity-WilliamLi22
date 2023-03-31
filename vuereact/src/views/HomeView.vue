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
          name: "Plain Roll",
          type: "Bread",
          image:
            "https://ipcdn.freshop.com/resize?url=https://images.freshop.com/7744242/3056f20cb20cfe25dc14ed5e195aacff_large.png&width=512&type=webp&quality=90",
          price: 2,
        },
        {
          name: "Bacon and Cheddar Roll",
          type: "Bread",
          image:
            "https://milkandpop.com/wp-content/uploads/2021/02/subway-bread-8.jpg",
          price: 3,
        },
        {
          name: "Lettuce",
          type: "Vegetable",
          image:
            "https://assets.bonappetit.com/photos/57e1807fbf7e91497a10e216/16:9/w_1280,c_limit/lettuce-640.jpg",
          price: 1,
        },
        {
          name: "Cucumber",
          type: "Vegetable",
          image:
            "https://t3.ftcdn.net/jpg/03/24/22/42360_F_324224284_KEgkz9bGAROme3X5j9k3ddwiHm3BE2IO.jpg",
          price: 1,
        },
        {
          name: "Tomato",
          type: "Vegetable",
          image:
            "https://s3.envato.com/files/3254570842019_09_Victor_food_IMG_0072-2-Edit_20190513.jpg",
          price: 1,
        },
        "Bacon $3",
        "Meatballs $3",
        "Grilled Chicken $3",
        "Ham $3",
        "Steak $4",
        {
          name: "Shredded Mozzarella",
          type: "Dairy Product",
          image:
            "https://www.foodservicedirect.com/media/catalog/product/1/0/10738824609105.jpg?width=1200&height=1200&quality=85&fit=bounds",
          price: 2,
        },
        {
          name: "Shredded Cheddar Cheese",
          type: "Dairy Product",
          image:
            "https://www.foodservicedirect.com/media/catalog/product/0/3/034500417471_1_yrhbjympw1gwmaw5.jpg?width=1200&height=1200&quality=85&fit=bounds",
          price: 2,
        },
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
