<template>
  <div>
    <h2>{{ name }}</h2>
    <h2>{{ type }}</h2>
    <img class="img" :src="image" alt="" />
    <h2>{{ price }}</h2>
    <button
      @click="
        order({
          name: name,
          type: type,
          image: image,
          price: price,
        })
      "
    >
      Add to cart
    </button>
  </div>
</template>

<script>
import { reactive } from "vue";
export const selected = reactive([]);
export default {
  name: "Card",
  props: {
    name: String,
    type: String,
    image: String,
    price: Number,
  },
  computed: {
    getImage: function () {
      return this.image;
    },
  },
  methods: {
    order: function (object) {
      selected.push(object);
      console.log(selected);
    },
  },
};
</script>

<style>
.card {
  width: 30%;
  height: 300px;
  margin: 10px auto;
  flex-wrap: wrap;
}
.img {
  height: 20%;
  width: 25%;
  object-fit: cover;
}
</style>
