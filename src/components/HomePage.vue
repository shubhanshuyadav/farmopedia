<template>
  <div id="app">
    <v-app id="inspire">
      <navbar/>
      <div id="header">
        <h1>Cheese Curds</h1>
        <p>Yes, please.</p>
        <v-btn
          class="ma-2"
          :loading="loading2"
          :disabled="loading2"
          color="success"
          @click="loader = 'loading2'"
        >
          <router-link
            style="text-decoration: none; color: white"
            to="/all-facilities"
            >Services</router-link
          >
        </v-btn>
      </div>
    </v-app>
  </div>
</template>

<script>
import Navbar from './Navbar.vue';
export default {
  name: "HomePage",
  components: {
    Navbar,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#header {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  text-align: center;
}
h1 {
  text-transform: uppercase;
  margin: 0;
  font-size: 3rem;
  white-space: nowrap;
}
p {
  margin: 0;
  font-size: 1.5rem;
}
#inspire {
  background: url("../assets/images/bg7.jpeg") no-repeat center center fixed !important;
}
.item {
  background-color: azure;
}
.logo {
  color: black;
  font-weight: 900;
  font-size: 1.8rem;
  padding-left: 5rem;
}
.v-list-group-active {
  color: green;
}
</style>
