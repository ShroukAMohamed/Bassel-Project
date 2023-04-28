<template>
  <div class="Courses">
    <div class="gray-img d-flex align-items-center overflow-hidden">
      <div class="container">
        <div class="row justify-content-center align-items-center">
          <div class="col-lg-8 col-12">
            <div class="course-details">
              <div
                class="course-img overflow-hidden d-flex flex-column justify-content-center"
              >
                <div class="overlay"></div>
                <div
                  class="position-relative h-100 d-flex justify-content-center flex-column"
                >
                  <div class="row justify-content-between">
                    <div
                      class="enroll col-6 col-md-5 d-flex flex-column flex-sm-row justify-content-center align-items-center pe-0 ps-0"
                    >
                      <div class="d-inline">
                        <span class="me-sm-1">
                          <i class="fa-solid fa-star"></i
                        ></span>
                        <span class="me-sm-1">
                          <i class="fa-solid fa-star"></i
                        ></span>
                        <span class="me-sm-1">
                          <i class="fa-solid fa-star"></i
                        ></span>
                        <span class="me-sm-1">
                          <i class="fa-solid fa-star"></i
                        ></span>
                      </div>
                      <span class="ms-sm-2">(100) enrollment</span>
                    </div>
                    <div
                      class="promo-code col-5 col-xl-3 col-md-4 d-flex flex-column justify-content-center align-items-center"
                    >
                      <span>#Promo Code:</span>
                      <span>WEDDEV</span>
                    </div>
                  </div>
                  <div
                    class="d-flex flex-column text-light justify-content-center align-items-center mt-sm-5 h-100"
                  >
                    <h3 class="text-center">Course Name Goes Here</h3>
                    <div class="text-style">
                      <p>
                        Mauris imperdiet orci dapibus, commodo libero nec,
                        interdum tortor. Morbi in nibh faucibus, iaculis lorem
                        Mauris imperdiet orci dapibus, commodo libero nec,
                        interdum tortor. Morbi in nibh faucibus, iaculis lorem
                      </p>
                    </div>
                    <div class="options">
                      <span
                        ><i class="fa-solid fa-laptop-code"></i> 4 Tracks</span
                      >
                      <span><i class="fa-solid fa-users"></i> 2 Group</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <section class="course-info pb-5">
      <div class="container">
        <div class="row text-center">
          <div class="col-12 pt-5 pb-5">
            <span class="spanColor"></span>
            <h2>Course Groups</h2>
          </div>
        </div>
        <div class="bg-card">
          <p class="ms-5 pt-5 Groups-text">
            <i class="fa-solid fa-users"></i> 3 Groups:
          </p>
          <div class="row justify-content-center">
            <GroupCard />
            <GroupCard />
          </div>

          <div class="Hide">
            <div class="row justify-content-center mt-3">
              <GroupCard />
              <GroupCard />
            </div>
          </div>

          <div class="d-flex justify-content-center">
            <button @click="showFunction" class="Showbtn">Load More</button>
          </div>
          <div class="d-flex justify-content-center">
            <button @click="hideFunction" class="Hidebtn">See Less</button>
          </div>
        </div>
      </div>
    </section>
    <FooterA />
  </div>
</template>

<script>
import $ from "jquery";
import FooterA from "../components/global/Footer.vue";
import GroupCard from "../components/CourseContent/GroupCard.vue";
export default {
  name: "CourseContent",
  components: { FooterA, GroupCard },
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
@import "../components/global/scss/main.scss";
.Courses {
  margin-top: 50px;
  .gray-img {
    background-image: url("../assets/Rectangle\ 485.svg");
    height: 80vh;
    @include imageFormat;
    position: relative;
    @include breakpoints(mobile) {
      height: 100vh;
    }
    .course-details {
      .course-img {
        position: relative;
        background-image: url("../assets/mr-bochelly-IBKyH0V3rew-unsplash@2x.png");
        background-position: center center;
        background-size: cover;
        width: 100%;
        height: 60vh;
        @include breakpoints(mobile) {
          background-position: 30% 100%;
          height: 80vh;
        }

        .overlay {
          @include overlays;
          background-color: rgba(0, 0, 0, 0.367);
        }
        .enroll {
          background-color: white;
          div {
            span {
              color: #ffb12b;
              @include breakpoints(mobile) {
                font-size: 16px;
              }
            }
          }
          > span:last-of-type {
            font-weight: 600;
            font-size: 18px;
            @include breakpoints(mobile) {
              font-size: 16px;
            }
          }
        }
        .promo-code {
          background-color: #2503f3;
          color: white;
          clip-path: polygon(25% 0%, 100% 0%, 100% 100%, 25% 100%, 0% 50%);
          span:last-of-type {
            font-weight: 600;
            letter-spacing: 1px;
            @include breakpoints(mobile) {
              font-size: 13px;
            }
          }
        }
        h3 {
          font-size: 34px;
          font-weight: bold;
          letter-spacing: 1px;
          @include breakpoints(mobile) {
            font-size: 25px;
          }
        }
        .text-style {
          font-size: 18px;
          width: 100%;
          max-width: 500px;
          margin: 20px 0;
          text-align: center;
          letter-spacing: 2px;
          font-weight: 400;
          @include breakpoints(mobile) {
            font-size: 14px;
          }
        }
        .options {
          span {
            padding: 0 30px;
            font-size: 18px;
            font-weight: bold;
            @include breakpoints(mobile) {
              font-size: 14px;
            }
          }
        }
      }
    }
  }
  .course-info {
    h2 {
      font-weight: 800;
      letter-spacing: 1px;
      position: relative;
      z-index: 3;
    }
    .spanColor {
      position: absolute;
      z-index: 1;
      width: 150px;
      height: 30px;
      background-color: #ffbc00;
      right: 48%;
      margin-top: 20px;
    }
    .Hidebtn {
      display: none;
    }
    .bg-card {
      background-color: #f1f1f1;
      button {
        border: 0;
        margin: 50px 0;
        background-color: #292341;
        color: white;
        width: 100%;
        max-width: 200px;
        padding: 10px 0;
        border-radius: 22px;
      }
      .Groups-text {
        font-size: 18px;
        font-weight: 600;
        letter-spacing: 1px;
      }
      .Hide {
        display: none;
      }
    }
  }
}
</style>
