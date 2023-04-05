<!-- <NotWelcome /> -->
<template>
  <!-- <div v-for="ingredient in ingredients" :key="ingredient.name">
    <h3>{{ ingredient.name }}</h3>
    <p>Type: {{ ingredient.type }}</p>
    <img
      :src="ingredient.image"
      :alt="ingredient.name"
      width="210"
      height="200"
    />
    <p>Price: ${{ ingredient.price }}</p>
    <Button @click="order" :key="ingredients">Add to Sandwich</Button>
  </div> -->
  <Card
    v-for="ingredient in ingredients"
    :key="ingredient.name"
    :name="ingredient.name"
    :type="ingredient.type"
    :image="ingredient.image"
    :price="ingredient.price"
  />
</template>
<!-- <script setup>
import NotWelcome from "../components/NotWelcome.vue";
</script> -->

<script>
import { store } from "../components/store.js";
import Card from "../components/card.vue";
export default {
  name: "home",
  props: {
    name: String,
    type: String,
    image: String,
    price: Number,
  },
  components: {
    store,
    Card,
  },
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
            "https://th.bing.com/th/id/R.f5e61e24242113915155574adc773fb7?rik=LU%2bjr1pbVa93Mg&riu=http%3a%2f%2ffreefoodphotos.com%2fimagelibrary%2fvegetables%2fsliced_cucumber.jpg&ehk=%2batsY09ztjW%2fSbnFl5aFpu3MXzsqQFxXOSE%2bqfg7Ig4%3d&risl=&pid=ImgRaw&r=0",
          price: 1,
        },
        {
          name: "Tomato",
          type: "Vegetable",
          image:
            "https://th.bing.com/th/id/OIP.A3KtH1IjV8MfpZ2CP6s9tgHaHa?pid=ImgDet&rs=1",
          price: 1,
        },
        {
          name: "Bacon",
          type: "Meat",
          image:
            "https://th.bing.com/th/id/OIP.8R1sTsu1fl2W1FbslA52aAHaFI?pid=ImgDet&rs=1",
          price: 3,
        },
        {
          name: "Meatballs",
          type: "Meat",
          image:
            "https://thumbs.dreamstime.com/b/baked-homemade-meatballs-isolated-white-background-baked-homemade-meatballs-194260878.jpg",
          price: 3,
        },
        {
          name: "Chicken",
          type: "Meat",
          image:
            "https://media.istockphoto.com/photos/heap-of-pulled-chicken-meat-on-white-picture-id1221237582?k=20&m=1221237582&s=612x612&w=0&h=jNogYAgk6nDGjpJNca36Zpeaby_BEgA8zCS1ovZfov0=",
          price: 3,
        },
        {
          name: "Ham",
          type: "Meat",
          image:
            "https://thumbs.dreamstime.com/b/sliced-ham-white-background-pork-ham-sliced-white-backgro-sliced-ham-white-background-pork-ham-sliced-white-background-127407650.jpg",
          price: 3,
        },
        {
          name: "Steak",
          type: "Meat",
          image:
            "https://thumbs.dreamstime.com/b/rare-beef-fillet-steak-sliced-white-background-chargrilled-33625288.jpg",
          price: 4,
        },
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
};
</script>

<style></style>
