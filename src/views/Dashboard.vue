<template>
  <div>
    <div class="dashboard-img">
      <div class="container">
        <div class="Container-div">
          <div class="row pt-5">
            <div class="col-lg-6 first-part">
              <div class="row justify-content-center">
                <div
                  class="col-md-6 col-10 d-flex flex-column justify-content-between"
                >
                  <h3>Your Dashboard</h3>
                  <img
                    class="img-fluid"
                    src="../assets/MaskGroup55-svg-svg.svg"
                    alt=""
                  />
                </div>
                <div class="col-md-6 col-12 gy-5 gy-md-0">
                  <AttendState />
                </div>
              </div>
              <div class="Card m-auto me-md-0 mt-5">
                <div
                  class="d-flex justify-content-between align-items-center pb-2"
                >
                  <h3>Coming Sessions</h3>
                  <div class="Arrows">
                    <p>
                      <span @click="prevSessions" class="me-1 Left Hide"
                        ><i class="fa-solid fa-chevron-left"></i
                      ></span>
                      this month
                      <span @click="nextSessions" class="ms-1 Right"
                        ><i class="fa-solid fa-chevron-right"></i
                      ></span>
                    </p>
                  </div>
                </div>
                <div class="line"></div>
                <div class="Sessions">
                  <div class="session active">
                    <SessionsDate />
                  </div>
                  <div class="session Hidden">
                    <SessionsDate />
                  </div>

                  <div class="session Hidden">
                    <SessionsDate />
                  </div>
                </div>
                <!-- <p>Open more</p> -->
              </div>
              <div class="Card m-auto me-md-0 mt-5">
                <h3 class="pb-2">Recommended Courses For You</h3>
                <div class="line"></div>
                <Recommended />
                <p class="mt-3">Open more</p>
              </div>
            </div>
            <div class="col-lg-6 gy-5 gy-lg-0">
              <div class="blue-Card p-1 pt-4 p-md-4">
                <div
                  class="d-flex flex-xl-row flex-column pb-1 align-items-center justify-content-xl-between courses-board"
                >
                  <h3>Your Courses <span class="ms-1">2</span></h3>
                  <div class="mt-4 mt-xl-0">
                    <input type="text" placeholder="Search" />
                    <span><i class="fa-solid fa-magnifying-glass"></i></span>
                  </div>
                </div>
                <CoursesOwned />
                <CoursesOwned />
              </div>
            </div>
          </div>
          <div class="lastline"></div>
          <RegistInfo />
        </div>
      </div>
    </div>
    <ReviewPopup />
    <AttendPopup />
  </div>
</template>

<script>
import ReviewPopup from "../components/Dashboard/Review.vue";
import AttendPopup from "../components/Dashboard/AttendPopup.vue";
import RegistInfo from "../components/Dashboard/Registered";
import CoursesOwned from "../components/Dashboard/CoursesOwned.vue";
import SessionsDate from "../components/Dashboard/SessionsDate.vue";
import AttendState from "../components/Dashboard/Attendance.vue";
import Recommended from "../components/Dashboard/Recommend.vue";
import $ from "jquery";
export default {
  name: "DashBoard",
  components: {
    ReviewPopup,
    AttendPopup,
    RegistInfo,
    CoursesOwned,
    SessionsDate,
    AttendState,
    Recommended,
  },
  mounted() {
    this.checkSlider();
  },
  methods: {
    checkSlider() {
      if ($(".Sessions > div").eq(0).hasClass("Hidden")) {
        $("span.Left").removeClass("Hide");
      } else {
        $("span.Left").addClass("Hide");
      }

      if ($(".Sessions > div").eq(2).hasClass("Hidden")) {
        $("span.Right").removeClass("Hide");
      } else {
        $("span.Right").addClass("Hide");
      }
    },
    nextSessions() {
      var com = this;
      $(".session.active").fadeOut(300, function () {
        $(this)
          .next(".session")
          .addClass("active")
          .removeClass("Hidden")
          .fadeIn();
        $(this).addClass("Hidden").removeClass("active");
        com.checkSlider();
      });
    },
    prevSessions() {
      var com = this;
      $(".session.active").fadeOut(300, function () {
        $(this)
          .prev(".session")
          .addClass("active")
          .removeClass("Hidden")
          .fadeIn();
        $(this).addClass("Hidden").removeClass("active");
        com.checkSlider();
      });
    },
  },
  watch: {
    function() {},
  },
};
</script>

<style lang="scss" scoped>
@import "../components/global/scss/main.scss";
.dashboard-img {
  background-image: url("../assets/Group281.svg");
  width: 100%;
  background-position: 100% 100%;
  .Container-div {
    margin-top: 74px;
    .Card {
      background-color: white;
      box-shadow: 0 0.5rem 3rem rgba(0, 0, 0, 0.15) !important;
      padding: 20px;
      width: 100%;
      margin: auto;
      border-radius: 15px;
      margin-right: 20px;
    }
    .line {
      border-bottom: 1px solid rgb(206, 205, 205);
    }
    .first-part {
      > div:first-child {
        > div:first-child {
          h3 {
            position: relative;
            &::before {
              content: "";
              position: absolute;
              width: 150px;
              height: 3px;
              background-color: orange;
              top: 100%;
              margin-top: 4px;
            }
          }
        }
      }

      .Card:nth-of-type(2):not(.dashboard-info .Card),
      .Card:nth-of-type(3) {
        max-width: 500px;
        margin-top: 40px;
        margin-bottom: 40px;
        @include breakpoints(small) {
          max-width: 600px;
        }
        h3 {
          @include breakpoints(mobile) {
            font-size: 18px;
          }
        }

        p:nth-child(1) {
          color: rgb(86, 86, 87);
          font-size: 17px;
          margin-bottom: 5px;
          @include breakpoints(mobile) {
            font-size: 14px;
          }
          span {
            cursor: pointer;
          }
        }
        .Hide {
          display: none;
        }
        > div:nth-child(3) {
          background-color: #dbddf780;
          padding: 20px;
          margin-top: 20px;
          .Hidden {
            display: none !important;
          }
        }

        p:nth-child(4) {
          color: #6864b9;
          margin: 5px 0;
          cursor: pointer;
        }
      }
      .Card:nth-of-type(3) {
        p:nth-child(3) {
          font-size: 18px;
          color: #515661;
          width: 100%;
          max-width: 300px;
          letter-spacing: 1px;
        }
      }
    }
    .blue-Card {
      background-color: #bddfeb;
      border-radius: 25px;
      .courses-board {
        h3 {
          font-weight: 600;
          font-size: 28px;
          span {
            background-color: white;
            color: #2596be;
            border-radius: 50%;
            padding: 4px 12px;
            font-size: 23px;
            font-weight: 600;
          }
        }
        div {
          background-color: white;
          display: flex;
          align-items: center;
          padding: 6px 20px;
          border-radius: 25px;
          width: 100%;
          max-width: 250px;
          input {
            border: 0;
            &:focus {
              outline: none;
            }
          }
        }
      }
    }
    > div.lastline {
      border-bottom: 1px solid rgb(163, 162, 162);
      margin-top: 50px;
      margin-bottom: 30px;
    }
  }
}
</style>
