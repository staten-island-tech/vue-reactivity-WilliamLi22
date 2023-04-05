<template>
  <div>
    <h2>{{ name }}</h2>
    <h2>{{ type }}</h2>
    <img :src="image" alt="" />
    <h2>{{ price }}</h2>
    <button @click="Remove(name)">Add to cart</button>
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
    Remove: function (object) {
      let item = selected.find((item) => item.ingredient === object);
      selected.splice(item, 1);
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
}
</style>
