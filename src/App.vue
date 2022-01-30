<template>
  <div class="bg-dark h-screen">
    <div class="flex" style="height: 88vh">
      <!-- Side Navbar -->
      <SideNav />
      <!-- Main Content -->
      <Main />
    </div>
    <Footer />
  </div>
</template>

<script>
import "./assets/tailwind.css";
import SideNav from "./components/SideNav.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    SideNav,
    Main,
    Footer,
  },
};
</script>
