<template>
  <div>
    <navbar/>
    <div id="header">
      <h1>Cheese Curds</h1>
      <p>Yes, please.</p>
    </div>
    <v-row class="my-15">
      <v-col class="pt-15 pb-10"
        ><facility-card title="Seasonable & Suitable" :src="require('../assets/images/suitable.jpeg')"></facility-card
      ></v-col>
      <v-col class="pt-15 pb-10">
        <facility-card title="Seeds" :src="require('../assets/images/seeds.jpeg')"></facility-card
      ></v-col>
      <v-col class="pt-15 pb-10"
        ><facility-card title="Irrigation" :src="require('../assets/images/irragation.jpeg')"></facility-card
      ></v-col>
      <v-col class="pt-15 pb-10"
        ><facility-card title="Machines & Tools" :src="require('../assets/images/machines.jpeg')"></facility-card
      ></v-col>
      <v-col class="pt-15 pb-10"
        ><facility-card title="Insurance" :src="require('../assets/images/insurance.jpeg')"></facility-card
      ></v-col>
    </v-row>
  </div>
</template>

<script>
import FacilityCard from "./FacilityCard.vue";
import Navbar from './Navbar.vue';
export default {
  name: "AllFacilities",
  components: {
    FacilityCard,
    Navbar,
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
#header {
  background-color: #347947;
  top: 0;
  left: 50%;
  width: 100%;
  color: white;
  text-align: center;
  padding: 50px 50px;
}
</style>
