<template>
  <div>
    <ordercart
      v-for="ingredient in selected"
      :key="ingredient"
      :name="ingredient.name"
      :type="ingredient.type"
      :image="ingredient.image"
      :price="ingredient.price"
    />
  </div>
</template>

<script>
import ordercart from "../components/ordercart.vue";
import { selected } from "../components/card.vue";
export default {
  name: "Card",
  components: { ordercart },
  computed: {
    getImage: function () {
      return this.image;
    },
  },
  data() {
    return { selected };
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
