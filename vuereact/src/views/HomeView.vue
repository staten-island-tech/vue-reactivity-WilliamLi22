<template>
  <main>
    <TheWelcome />
  </main>
  <div class="Home">
    <!--  <h1 v-if="graduated">{{ student }}</h1>
    <h1 v-else>"They did not yet graduate"</h1>
    <ul>
      <li v-for="animal in animals" :key="animal">{{ animal }}</li>
    </ul> -->
    <button v-on:click="authState" v-if="loggedIn">Log Out</button>
    <button v-on:click="authState" v-else>Login</button>
  </div>
</template>

<script>
import TheWelcome from "../components/TheWelcome.vue";

export default {
  name: "Home",
  components: {},
  data() {
    return {
      loggedIn: false,
      /*    student: "Harry",
      graduated: true,
      animals: ["Pig", "Horse", "Donkey", "Cow", "Duck"], */
    };
  },
  methods: {
    authState: function () {
      if (this.loggedIn === false) {
        this.loggedIn === true;
      } else {
        this.loggedIn = false;
      }
    },
  },
};
</script>

<style scoped></style>
<!-- scoped makes it so that in this case, the style only applies to this file v-base
creates template
 -->
