<template>
  <div>
    <section class="courses block" id="Courses">
      <div class="courses-img">
        <div class="container">
          <div class="row justify-content-lg-center">
            <div class="col-12 order-first text-center gy-4 mb-4 mb-md-5">
              <h2>Available Courses</h2>
            </div>
            <div
              data-aos="fade-in"
              data-aos-duration="1000"
              class="col-lg-5 col-md-6 gy-4 order-2 order-md-1 col-12"
            >
              <AvCourses :name="course_name" :details="course_details" />
            </div>
            <div
              data-aos="zoom-in"
              data-aos-duration="1000"
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
          <div
            data-aos="fade-in"
            data-aos-duration="1000"
            class="row justify-content-center align-items-center pt-5"
          >
            <div class="col-lg-5 col-md-6 col-12">
              <AvCourses :name="course_name" :details="course_details" />
            </div>
            <div class="col-lg-5 col-md-6 col-12 gy-5 gy-md-0">
              <AvCourses :name="course_name" :details="course_details" />
            </div>
          </div>
          <div class="Hide">
            <div
              data-aos="fade-in"
              data-aos-duration="1000"
              class="row justify-content-center align-items-center pt-5"
            >
              <div class="col-lg-5 col-md-6 col-12">
                <AvCourses :name="course_name" :details="course_details" />
              </div>
              <div class="col-lg-5 col-md-6 col-12 gy-5 gy-md-0">
                <AvCourses :name="course_name" :details="course_details" />
              </div>
            </div>
            <div
              data-aos="fade-in"
              data-aos-duration="1000"
              class="row justify-content-center align-items-center pt-5"
            >
              <div class="col-lg-5 col-md-6 col-12">
                <AvCourses :name="course_name" :details="course_details" />
              </div>
              <div class="col-lg-5 col-md-6 col-12 gy-5 gy-md-0">
                <AvCourses :name="course_name" :details="course_details" />
              </div>
            </div>
          </div>
          <div class="text-center mt-5">
            <button
              @click="showFunction('.Hide', '.Showbtn', '.Hidebtn')"
              class="Showbtn"
            >
              See More
            </button>
          </div>
          <div class="text-center mt-5">
            <button
              @click="hideFunction('.Hide', '.Showbtn', '.Hidebtn')"
              class="Hidebtn"
            >
              See Less
            </button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import AvCourses from "./AvailableCourses/AvCourses.vue";
import show_btn from "../../../mixin/show_btn.vue";
export default {
  name: "CoursesComponent",
  components: { AvCourses },
  data() {
    return {
      course_name: "Web Develpment",
      course_details:
        "Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi in nibh faucibus, iaculis lorem vitae, cursus velit.",
    };
  },
  mixins: [show_btn],
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
.courses {
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
      font-size: 40px;
      letter-spacing: 1px;
      font-family: "Poppins", sans-serif;
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
        transition: all 0.3s;
        &:hover {
          transform: translateY(-6px);
        }
      }
    }
    .Hidebtn {
      display: none;
    }
  }
}
</style>
