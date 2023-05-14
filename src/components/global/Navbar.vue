<template>
  <div class="Navbar">
    <nav class="navbar navbar-expand-lg w-100 position-fixed top-0 pt-3">
      <div class="container">
        <router-link to="/" class="brand"></router-link>
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
              <li @mouseover="ActiveLink" class="nav-item">
                <router-link
                  data-scroll="Home"
                  to="/"
                  class="nav-link Active"
                  aria-current="page"
                  >Home</router-link
                >
              </li>
              <li @mouseover="ActiveLink" class="nav-item">
                <a data-scroll="Services" class="nav-link" href="/#Services"
                  >Services</a
                >
              </li>
              <li @mouseover="ActiveLink" class="nav-item">
                <a data-scroll="Courses" class="nav-link" href="/#Courses"
                  >Courses</a
                >
              </li>
              <li @mouseover="ActiveLink" class="nav-item">
                <a data-scroll="Projects" class="nav-link" href="/#Projects"
                  >Projects</a
                >
              </li>
              <li @mouseover="ActiveLink" class="nav-item">
                <a data-scroll="Jobs" class="nav-link" href="/#Jobs">Jobs</a>
              </li>
              <li @mouseover="ActiveLink" class="nav-item">
                <a data-scroll="About" class="nav-link" href="/#About">About</a>
              </li>
              <li @mouseover="ActiveLink" class="nav-item">
                <a data-scroll="Contact" class="nav-link" href="/#Contact"
                  >Contact</a
                >
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
import $ from "jquery";
export default {
  name: "NavBar",
  mounted() {
    // $("body").css("paddingTop", $(".Navbar").innerHeight());
    $(window).scroll(function () {
      $(".block").each(function () {
        if ($(window).scrollTop() > $(this).offset().top - 80) {
          var blockID = $(this).attr("id");
          $(".Navbar a").removeClass("Active");
          $('.Navbar li a[data-scroll="' + blockID + '"]').addClass("Active");
        }
      });
    });
  },
  methods: {
    ActiveLink() {
      $(".Navbar li a").click(function () {
        $(this)
          .addClass("Active")
          .parent()
          .siblings()
          .find("a")
          .removeClass("Active");
      });
    },
  },
};
</script>

<style lang="scss">
.Navbar {
  nav {
    z-index: 10;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(251, 249, 249, 0.91);
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
        .nav-link {
          color: rgb(120, 118, 118);
          transition: all 0.3s;
          font-size: 17px;
          &:hover {
            transform: translateY(-2px);
            color: black;
          }
        }

        a.Active {
          color: black;
        }
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
