<!-- <NotWelcome /> -->
<template>
  <div class="home">
    <h2>{{ now }}</h2>
  </div>
</template>

<!-- <script setup>
import NotWelcome from "../components/NotWelcome.vue";
</script> -->

<script>
import Button from "../components/Button.vue";
export default {
  name: "home",
  components: {
    Button,
  },
  data() {
    return {
      message: "",
    };
  },
  computed: {
    now: function () {
      const time = new Date();
      return `${time.getHours()}:${time.getMinutes()}`;
    },
  },
  methods: {},
};
</script>

<style scoped></style>
