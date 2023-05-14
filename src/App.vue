<template>
  <div id="app">
    <!-- <NavBar /> -->
    <router-view />
  </div>
</template>

<style lang="scss">
html,
body {
  overflow-x: hidden;
  scroll-behavior: smooth;
}
@import url("https://fonts.googleapis.com/css2?family=Asap:wght@500&family=Poppins:wght@600&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;500;700&display=swap");
</style>

<script>
import Vue from "vue";
Vue.mixin({
  mounted() {
    window.scrollTo(0, 0);
  },
});
// import NavBar from "@/components/global/Navbar.vue";
export default {
  // components: { NavBar },
  mounted() {
    // if (document.URL.indexOf("/Instructor")) {
    //   $(".Navbar").addClass("d-none");
    // } else {
    //   $(".Navbar").removeClass("d-none");
    // }
    let script = document.createElement("script");
    script.setAttribute(
      "src",
      "https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"
    );
    document.head.appendChild(script);
  },
};
</script>
