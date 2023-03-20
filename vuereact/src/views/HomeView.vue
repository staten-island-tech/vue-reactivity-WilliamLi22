<template>
  <NotWelcome />
  <div class="home">
    <input type="text" placeholder="Edit Me" />
    <p>{{ message }}</p>
  </div>
</template>

<script>
import NotWelcome from "../components/NotWelcome.vue";

export default {
  name: "Home",
  components: {},
  data() {
    return {
      message: "",
    };
  },
  methods: {},
};
</script>

<style scoped></style>
<!-- scoped makes it so that in this case, the style only applies to this file v-base
creates template
 -->
