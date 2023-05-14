<template>
  <div class="Instructor">
    <GroupPopup />
    <div class="navigation">
      <ul class="ps-2">
        <li class="logo">
          <router-link to="/">
            <span class="icon"
              ><img src="../assets/Logo-Png_64.png" alt=""
            /></span>
            <span class="title fw-bold mt-1">Bassel Allam</span>
          </router-link>
        </li>

        <li class="hovered activeHome">
          <a href="#">
            <span class="icon">
              <i class="fa-solid fa-house"></i>
            </span>
            <span class="title">Home</span>
          </a>
        </li>

        <li class="activeTask">
          <a href="#">
            <span class="icon"><i class="fa-solid fa-user-check"></i></span>
            <span class="title">Student Task</span>
          </a>
        </li>

        <li class="activePayment">
          <a href="#">
            <span class="icon"
              ><i class="fa-solid fa-money-check-dollar"></i
            ></span>
            <span class="title">Payment</span>
          </a>
        </li>

        <li class="activeCourses">
          <a href="#">
            <span class="icon"
              ><i class="fa-solid fa-chalkboard-user"></i
            ></span>
            <span class="title">Courses</span>
          </a>
        </li>
      </ul>
    </div>

    <div class="main">
      <div class="topbar">
        <div @click="activeMenu" class="toggle">
          <i class="fa-solid fa-bars"></i>
        </div>
        <div class="Text">
          <h3 class="mb-0 d-none d-sm-block">Welcome Back Jerry</h3>
        </div>
        <div class="user d-flex align-items-center me-3">
          <img class="me-3" src="../assets/cheif1.jpg" alt="" />
          <div class="d-flex flex-column">
            <span class="fw-bold">Jerry Garret</span>
            <span>Instructor</span>
          </div>
        </div>
      </div>
      <div class="bg-image">
        <div class="HomeSection pt-5">
          <HomeSection />
        </div>
        <div class="TaskSection pt-5 d-none">
          <TaskSection />
        </div>
        <div class="PaymentSection pt-5 d-none">
          <PaymentSection />
        </div>
        <div class="CoursesSection d-none">
          <CourseSection />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";
import CourseSection from "@/components/Instructor/CoursesSection.vue";
import TaskSection from "@/components/Instructor/TaskSection.vue";
import GroupPopup from "@/components/Instructor/CoursesSection/GroupPopup.vue";
import HomeSection from "@/components/Instructor/HomeSection.vue";
import PaymentSection from "@/components/Instructor/PaymentSection.vue";
export default {
  name: "IstructorDashboard",

  components: {
    GroupPopup,
    HomeSection,
    TaskSection,
    PaymentSection,
    CourseSection,
  },
  mounted() {
    $(".navigation li").click(function () {
      $(this).addClass("hovered").siblings().removeClass("hovered");
    });
    $(".activeHome").click(function () {
      $(".HomeSection").removeClass("d-none").siblings().addClass("d-none");
    });
    $(".activeTask").click(function () {
      $(".TaskSection").removeClass("d-none").siblings().addClass("d-none");
    });
    $(".activePayment").click(function () {
      $(".PaymentSection").removeClass("d-none").siblings().addClass("d-none");
    });
    $(".activeCourses").click(function () {
      $(".CoursesSection").removeClass("d-none").siblings().addClass("d-none");
    });
  },
  methods: {
    activeMenu() {
      $(".navigation").toggleClass("active");
      $(".main").toggleClass("active");
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../components/global/scss/main.scss";
.Instructor {
  font-family: "Ubuntu", sans-serif;
  width: 100%;

  .navigation.active {
    width: 80px;
    @include breakpoints(medium) {
      width: 250px;
      left: 0;
    }
    @include breakpoints(smaller) {
      width: 100%;
      left: 0;
    }
  }
  .navigation {
    position: fixed;
    width: 300px;
    height: 100%;
    background-color: #1086ed;
    transition: 0.5s;
    overflow: hidden;
    @include breakpoints(medium) {
      left: -250px;
      width: 250px;
    }
    @include breakpoints(smaller) {
      width: 100%;
      left: -100%;
      z-index: 200;
      transition: 0.3s;
    }
    ul {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      li.hovered {
        a {
          color: #147ad6;
        }
      }
      li {
        position: relative;
        width: 100%;
        list-style: none;
        border-top-left-radius: 30px;
        border-bottom-left-radius: 30px;
        margin: 10px 0;
        &:not(:nth-child(1)):hover,
        &.hovered:not(:nth-child(1)) {
          background-color: white;
          a::before {
            content: "";
            position: absolute;
            right: 0;
            top: -50px;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            box-shadow: 35px 35px 0 10px white;
            background-color: transparent;
            pointer-events: none;
          }
          a::after {
            content: "";
            position: absolute;
            right: 0;
            bottom: -50px;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            box-shadow: 35px -35px 0 10px white;
            background-color: transparent;
            pointer-events: none;
          }
        }
        a {
          position: relative;
          display: block;
          width: 100%;
          display: flex;
          text-decoration: none;
          color: white;
          &:not(.logo a):hover {
            color: #147ad6;
          }
          .icon {
            position: relative;
            display: block;
            min-width: 60px;
            height: 60px;
            line-height: 60px;
            text-align: center;
            font-size: 22px;
          }
          .title {
            position: relative;
            display: block;
            padding-left: 15px;
            height: 60px;
            line-height: 60px;
            text-align: start;
            white-space: nowrap;
          }
        }
      }
      li:nth-child(1) {
        margin-bottom: 40px;
        font-size: 18px;
      }
    }
  }
  .main.active {
    width: calc(100% - 80px);
    left: 80px;

    @include breakpoints(medium) {
      left: 250px;
    }
    @include breakpoints(smaller) {
      left: 0;
      width: 100%;

      .toggle {
        color: white !important;
        position: fixed !important;
        left: initial !important;
        right: 0 !important;
      }
    }
  }
  .main {
    position: absolute;
    width: calc(100% - 300px);
    left: 300px;
    background-color: white;
    transition: 0.5s;
    @include breakpoints(medium) {
      width: 100%;
      left: 0;
    }
    .topbar {
      box-shadow: 0px 3px 12px #00000029;
      width: 100%;
      height: 85px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 10px;
      .toggle {
        position: relative;
        width: 60px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 30px;
        cursor: pointer;
        color: black;
        @include breakpoints(smaller) {
          z-index: 201;
        }
      }

      .Text {
        font-family: "Poppins", serif;
      }

      .user {
        position: relative;
        overflow: hidden;
        @include breakpoints(smaller) {
          min-width: 40px;
        }
        img {
          position: relative;
          top: 0;
          left: 0;
          width: 48px;
          object-fit: cover;
          height: 48px;
          border-radius: 50%;
        }
      }
    }

    .bg-image {
      background-image: url("../assets/Group281.svg");
      width: 100%;

      .HomeSection {
      }
      .TaskSection {
      }

      .PaymentSection {
      }
      .CoursesSection {
        display: flex;
        align-items: center;
        padding-top: 80px;
        padding-bottom: 50px;
      }
    }
  }
}
</style>
