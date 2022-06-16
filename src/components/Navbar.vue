<template>
  <div>
    <v-toolbar app dark color="white" class="hidden-xs-and-down" height="80px">
      <v-toolbar-title class="logo">Farmopedia</v-toolbar-title>
      <v-spacer></v-spacer>
      <router-link
        v-for="item in nav"
        :key="item.icon"
        :title="item.title"
        class="link"
        :to="item.route"
        >{{ item.text }}</router-link
      >
    </v-toolbar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      dialog: false,
      nav: [
        {
          route: "/",
          icon: "home",
          text: "Home",
          title: "Back to Home page",
          active: true,
        },
        {
          route: "/about",
          icon: "info",
          text: "About",
          title: "About our work",
          active: false,
        },
        {
          route: "/all-facilities",
          icon: "assignment_turned_in",
          text: "Facilities",
          title: "Some stuff that we doing",
          active: false,
        },
        {
          route: "/contact",
          icon: "email",
          text: "Contact",
          title: "Our Contact info",
          active: false,
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
.link {
  text-decoration: none;
  color: black;
  padding: 25px 25px;
  font-size: 1.2rem;
  font-weight: 450;
}
.link:hover {
  background: green;
  color: aliceblue;
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
</style>
