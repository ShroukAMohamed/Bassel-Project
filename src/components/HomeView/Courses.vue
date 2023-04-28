<template>
  <div>
    <section class="courses">
      <div class="courses-img">
        <div class="container">
          <div class="row justify-content-lg-center">
            <div class="col-12 order-first text-center gy-4 mb-4 mb-md-5">
              <h2>Available Courses</h2>
            </div>
            <div class="col-lg-5 col-md-6 gy-4 order-2 order-md-1 col-12">
              <AvCourses />
            </div>
            <div
              class="col-md-5 col-12 d-flex gy-4 order-md-last order-1 justify-content-center align-items-center"
            >
              <div class="course-text">
                <p>
                  Mauris imperdiet orci dapibus, commodo libero nec, interdum
                  tortor. Morbi in nibh faucibus, iaculis lorem vitae,Mauris
                  imperdiet orci dapibus, commodo libero nec, interdum tortor.
                  Morbi in nibh faucibus, iaculis lorem vitae.
                </p>
                <p>Explore & Enroll Now</p>
              </div>
            </div>
          </div>
          <div class="row justify-content-center align-items-center pt-5">
            <div class="col-lg-5 col-md-6 col-12">
              <AvCourses name="web development" />
            </div>
            <div class="col-lg-5 col-md-6 col-12 gy-5 gy-md-0">
              <AvCourses :name="course_name" />
            </div>
          </div>
          <div class="Hide">
            <div class="row justify-content-center align-items-center pt-5">
              <div class="col-lg-5 col-md-6 col-12">
                <AvCourses name="flutter" />
              </div>
              <div class="col-lg-5 col-md-6 col-12 gy-5 gy-md-0">
                <AvCourses />
              </div>
            </div>
            <div class="row justify-content-center align-items-center pt-5">
              <div class="col-lg-5 col-md-6 col-12">
                <AvCourses name="abc" />
              </div>
              <div class="col-lg-5 col-md-6 col-12 gy-5 gy-md-0">
                <AvCourses name="secuity" />
              </div>
            </div>
          </div>
          <div class="col-12 text-center mt-5">
            <button @click="showFunction" class="Showbtn">See More</button>
          </div>
          <div class="col-12 text-center mt-5">
            <button @click="hideFunction" class="Hidebtn">See Less</button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import $ from "jquery";
import AvCourses from "./AvailableCourses/AvCourses.vue";
export default {
  name: "CoursesComponent",
  components: { AvCourses },
  data() {
    return {
      course_name: "test course",
    };
  },
  methods: {
    showFunction() {
      $(".Hide").fadeIn();
      $(".Showbtn").hide();
      $(".Hidebtn").show();
    },
    hideFunction() {
      $(".Hide").fadeOut();
      $(".Showbtn").show();
      $(".Hidebtn").hide();
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
.courses {
  margin-bottom: 30px;
  .courses-img {
    background-image: url("../../assets/Group281.svg");
    width: 100%;
    background-position: 100% 100%;
    @include breakpoints(mobile) {
      background-size: cover;
    }
    .Hide {
      display: none;
    }
    h2 {
      font-weight: bold;
      font-size: 45px;
      letter-spacing: 1px;
      @include breakpoints(mobile) {
        font-size: 35px;
      }
    }

    .course-text {
      width: 90%;
      max-width: 450px;
      margin: auto;
      p:first-of-type {
        font-size: 18px;
        font-weight: 600;
        color: #515661;
      }
      p:last-of-type {
        font-size: 18px;
        font-weight: bold;
        color: black;
      }
    }
    div {
      button:first-child {
        border: 0;
        background-color: transparent;
        padding: 10px 60px;
        color: whitesmoke;
        font-size: 14px;
        letter-spacing: 1px;
        background: transparent
          linear-gradient(180deg, #2596be 0%, #2503f3 100%) 0% 0% no-repeat
          padding-box;
        box-shadow: 0px 3px 6px #292341;
        border-radius: 18px;
        opacity: 1;
      }
    }
    .Hidebtn {
      display: none;
    }
  }
}
</style>
