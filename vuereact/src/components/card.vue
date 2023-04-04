<template>
  <div>
    <h2>{{ name }}</h2>
    <h2>{{ type }}</h2>
    <img :src="image" alt="" />
    <h2>{{ price }}</h2>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    name: String,
    type: String,
    image: String,
    price: String,
  },
};
</script>

<style scoped></style>
