<template>
  <div>
    <div id="app">
      <navbar/>
      <div id="header">
      <h1>Cheese Curds</h1>
      <p>Yes, please.</p>
    </div>
      <v-app >
        <v-layout justify-center>
          <v-flex xs12 sm10 md8 lg6>
            <v-card class="mt-10" max-width="800">
              <v-card-text>
                <v-text-field
                  ref="name"
                  color="#347947"
                  v-model="name"
                  :rules="[() => !!name || 'This field is required']"
                  :error-messages="errorMessages"
                  label="Full Name"
                  required
                  @update:error="updateError()"
                ></v-text-field>
                <v-text-field
                  ref="address"
                  color="#347947"
                  :rules="[
                    () => !!address || 'This field is required',
                    () =>
                      (!!address && address.length <= 25) ||
                      'Address must be less than 25 characters',
                    addressCheck,
                  ]"
                  v-model="address"
                  label="Address Line"
                  counter="25"
                  required
                ></v-text-field>
                <v-text-field
                  ref="city"
                  color="#347947"
                  :rules="[
                    () => !!city || 'This field is required',
                    addressCheck,
                  ]"
                  v-model="city"
                  label="City"
                  required
                ></v-text-field>
                <v-text-field
                  ref="state"
                  color="#347947"
                  v-model="state"
                  :rules="[() => !!state || 'This field is required']"
                  label="State/Province/Region"
                  required
                ></v-text-field>
                <v-text-field
                  ref="zip"
                  color="#347947"
                  :rules="[() => !!zip || 'This field is required']"
                  v-model="zip"
                  label="ZIP / Postal Code"
                  required
                ></v-text-field>
              </v-card-text>
              <v-divider class="mt-5"></v-divider>
              <v-card-actions>
                <v-btn flat>Cancel</v-btn>
                <v-spacer></v-spacer>
                <v-slide-x-reverse-transition>
                  <v-tooltip v-if="formHasErrors" left>
                    <v-btn
                      slot="activator"
                      icon
                      class="my-0"
                      @click="resetForm"
                    >
                      <v-icon>refresh</v-icon>
                    </v-btn>
                    <span>Refresh form</span>
                  </v-tooltip>
                </v-slide-x-reverse-transition>
                <v-btn color="primary" flat @click="submit">Submit</v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-app>
    </div>
  </div>
</template>

<script>
import Navbar from './Navbar.vue';
export default {
  name: "Contact",
  components: {
    Navbar,
  }
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
.custom-placeholer-color input::placeholder {
  color: #347947!important;
  opacity: 1;
}

</style>
