<template>
  <div class="container">
    <div class="row align-items-stretch">
      <h2 class="text-center">Your Assigned Courses</h2>
      <div class="col-lg-4 col-md-6 d-flex justify-content-center">
        <div class="CourseCard cardStyle">
          <CourseCard />
          <button
            data-bs-target="#GroupModal"
            data-bs-toggle="modal"
            data-bs-dismiss="modal"
            class="ms-5 btn btn-outline-primary"
          >
            See Details
          </button>
        </div>
      </div>
      <div class="col-lg-4 col-md-6 d-flex justify-content-center gy-5 gy-md-0">
        <div class="CourseCard cardStyle">
          <CourseCard />
          <button
            data-bs-target="#GroupModal"
            data-bs-toggle="modal"
            data-bs-dismiss="modal"
            class="ms-5 btn btn-primary"
          >
            See Details
          </button>
        </div>
      </div>
      <div class="col-lg-4 d-flex justify-content-center gy-5 gy-lg-0">
        <div class="CourseCard cardStyle">
          <CourseCard />
          <button
            data-bs-target="#GroupModal"
            data-bs-toggle="modal"
            data-bs-dismiss="modal"
            class="ms-5 btn btn-outline-primary"
          >
            See Details
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CourseCard from "./CoursesSection/Course_Card.vue";
export default {
  name: "CoursesSection",
  components: { CourseCard },
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
.container {
  h2 {
    margin-bottom: 80px;
    font-size: 38px;
    font-family: "Poppins", serif;
    @include breakpoints(mobile) {
      margin-bottom: 40px;
      font-size: 32px;
    }
  }

  .cardStyle {
    border-top: 4px solid #0d6efd;
  }
  .CourseCard {
    background-color: white;
    box-shadow: 0px 3px 15px #00000029;
    padding: 50px 0;
    border-radius: 15px;
    width: 100%;
    max-width: 350px;
    @include breakpoints(small) {
      max-width: 450px;
    }
    button {
      width: 100%;
      max-width: 150px;
      margin-top: 15px;
      padding: 8px 0;
      font-weight: 500;
      border-radius: 20px;
    }
  }
}
</style>
