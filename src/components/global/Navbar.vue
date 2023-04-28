<template>
  <div class="Navbar">
    <ContactUs />
    <nav
      class="navbar navbar-expand-lg w-100 position-fixed top-0 pt-3 bg-light"
    >
      <div class="container">
        <div class="brand"></div>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarScroll"
          aria-controls="navbarScroll"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarScroll">
          <div class="d-lg-flex justify-content-lg-end w-100">
            <ul class="navbar-nav navbar-nav-scroll">
              <li class="nav-item">
                <router-link to="/" class="nav-link active" aria-current="page"
                  >Home</router-link
                >
              </li>
              <li class="nav-item">
                <a
                  class="nav-link"
                  href="#"
                  data-bs-target="#contactModal"
                  data-bs-toggle="modal"
                  data-bs-dismiss="modal"
                  >Contact Us</a
                >
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Our Service</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Courses</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Privacy Policy</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- <div class="line m-auto"></div> -->
    </nav>
  </div>
</template>

<script>
import ContactUs from "./ContactUs.vue";
export default {
  name: "NavBar",
  components: { ContactUs },
};
</script>

<style lang="scss" scoped>
.Navbar {
  nav {
    z-index: 10;
    display: flex;
    justify-content: center;
    align-items: center;
    .brand {
      background-image: url("@/assets/Full-Logo.png");
      width: 150px;
      height: 50px;
      background-size: cover;
      background-position: 100% 100%;
    }
    ul {
      li {
        padding: 0px 20px;
        font-weight: 600;
      }
    }
  }
}
</style>

<!-- <style lang="scss" scoped>
</style> -->
<!-- .line {
  border-bottom: 0.9px solid grey;
  width: 55%;
  position: absolute;
  bottom: 8%;
  left: 23%;
} -->
