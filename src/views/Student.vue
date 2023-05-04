<template>
  <div>
    <div class="dashboard-img">
      <div class="container">
        <div class="Container-div">
          <div class="row pt-5">
            <div
              data-aos="fade-right"
              data-aos-duration="1000"
              class="col-lg-6 first-part"
            >
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
                  <div class="Card m-auto">
                    <h3>Attendance</h3>
                    <div class="line"></div>
                    <AttendState
                      :Course_Name="Course_Name"
                      :Session_Num="Session_Num"
                      :Completion="Completion"
                    />
                    <div class="line"></div>
                    <AttendState
                      :Course_Name="Course_Name"
                      :Session_Num="Session_Num"
                      :Completion="Completion"
                    />
                  </div>
                </div>
              </div>
              <div class="Card m-auto me-md-0 mt-5">
                <div
                  class="d-flex flex-column flex-sm-row justify-content-between align-items-center pb-2"
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
                    <SessionsDate
                      :Course_Title="Course_Title"
                      :Track_Title="Track_Title"
                      :Session_Date="Session_Date"
                    />
                  </div>
                  <div class="session Hidden">
                    <SessionsDate
                      :Course_Title="Course_Title"
                      :Track_Title="Track_Title"
                      :Session_Date="Session_Date"
                    />
                  </div>

                  <div class="session Hidden">
                    <SessionsDate
                      :Course_Title="Course_Title"
                      :Track_Title="Track_Title"
                      :Session_Date="Session_Date"
                    />
                  </div>
                  <div class="session Hidden">
                    <SessionsDate
                      :Course_Title="Course_Title"
                      :Track_Title="Track_Title"
                      :Session_Date="Session_Date"
                    />
                  </div>
                </div>
                <!-- <p>Open more</p> -->
              </div>
              <div class="Card m-auto me-md-0 mt-5">
                <h3 class="pb-2">Recommended Courses For You</h3>
                <div class="line"></div>
                <Recommended
                  :CourseNameR="CourseNameR"
                  :DetailsR="DetailsR"
                  :Num_Tracks="Num_Tracks"
                  :Num_Groups="Num_Groups"
                />
                <div class="HideRecommend">
                  <Recommended
                    :CourseNameR="CourseNameR"
                    :DetailsR="DetailsR"
                    :Num_Tracks="Num_Tracks"
                    :Num_Groups="Num_Groups"
                  />
                  <Recommended
                    :CourseNameR="CourseNameR"
                    :DetailsR="DetailsR"
                    :Num_Tracks="Num_Tracks"
                    :Num_Groups="Num_Groups"
                  />
                </div>
                <div class="mt-3">
                  <a
                    @click="
                      showFunction('.HideRecommend', '.ShowRe', '.HideRe')
                    "
                    class="ShowRe"
                    >Open more</a
                  >
                  <a
                    @click="
                      hideFunction('.HideRecommend', '.ShowRe', '.HideRe')
                    "
                    class="HideRe"
                    >Open less</a
                  >
                </div>
              </div>
            </div>
            <div
              data-aos="fade-left"
              data-aos-duration="1000"
              class="col-lg-6 gy-5 gy-lg-0"
            >
              <div class="blue-Card p-1 pt-4 p-md-4">
                <div
                  class="d-flex flex-xl-row flex-column pb-1 align-items-center justify-content-xl-between StudentCourses"
                >
                  <h3>
                    Your Courses <span class="ms-1">{{ Courses_Owned }}</span>
                  </h3>
                  <div class="mt-4 mt-xl-0">
                    <input type="text" placeholder="Search" />
                  </div>
                </div>
                <CoursesOwned
                  :Course_Name="Course_Name"
                  :Session_Num="Session_Num"
                  :Completion="Completion"
                  :TrackInfo="TrackInfo"
                  :TrackDetails="TrackDetails"
                  :Group="Group"
                  :GroupStatus="GroupStatus"
                  :FromDate="FromDate"
                  :ToDate="ToDate"
                  :Duration="Duration"
                  :CourseLocation="CourseLocation"
                  :MaxCapacity="MaxCapacity"
                />
                <CoursesOwned
                  :Course_Name="Course_Name"
                  :Session_Num="Session_Num"
                  :Completion="Completion"
                  :TrackInfo="TrackInfo"
                  :TrackDetails="TrackDetails"
                  :Group="Group"
                  :GroupStatus="GroupStatus"
                  :FromDate="FromDate"
                  :ToDate="ToDate"
                  :Duration="Duration"
                  :CourseLocation="CourseLocation"
                  :MaxCapacity="MaxCapacity"
                />
              </div>
            </div>
          </div>
          <div class="lastline"></div>
          <RegistInfo
            :Full_Name="Full_Name"
            :Email="Email"
            :PhoneـNumber="PhoneـNumber"
            :DetailedـAddress="DetailedـAddress"
            :Birth_Date="Birth_Date"
          />
        </div>
      </div>
    </div>
    <ReviewPopup />
    <AttendPopup :Session_Num="Session_Num" :Completion="Completion" />
  </div>
</template>

<script>
import ReviewPopup from "../components/Student/Review.vue";
import AttendPopup from "../components/Student/AttendPopup.vue";
import RegistInfo from "../components/Registered.vue";
import CoursesOwned from "../components/Student/CoursesOwned.vue";
import SessionsDate from "../components/Student/SessionsDate.vue";
import AttendState from "../components/Student/Attendance.vue";
import Recommended from "../components/Student/Recommend.vue";
import $ from "jquery";
import show_btn from "../../mixin/show_btn.vue";
export default {
  name: "StudentDashboard",
  data() {
    return {
      Course_Name: "Course Name",
      Session_Num: "20/50",
      Completion: "60%",
      Course_Title: "Course Title here",
      Track_Title: "Track Title here",
      Session_Date: "Mon 9:30 am",
      CourseNameR: "Course Title here",
      DetailsR:
        "Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi in nibh faucibus,",
      Num_Tracks: "4 Tracks",
      Num_Groups: "2 Groups",
      Courses_Owned: "2",
      TrackInfo: "TrackInfo",
      TrackDetails: "TrackDetails",
      Group: "Group",
      GroupStatus: "GroupStatus",
      FromDate: "FromDate",
      ToDate: "ToDate",
      Duration: "Duration",
      CourseLocation: "CourseLocation",
      MaxCapacity: "MaxCapacity",
      Full_Name: "Full Name",
      Email: "Email",
      PhoneـNumber: "Phone Number",
      DetailedـAddress: "Detailed Address",
      Birth_Date: "Date of birth",
    };
  },
  components: {
    ReviewPopup,
    AttendPopup,
    RegistInfo,
    CoursesOwned,
    SessionsDate,
    AttendState,
    Recommended,
  },
  mixins: [show_btn],
  mounted() {
    this.checkSlider();
  },
  methods: {
    checkSlider() {
      if ($(".Sessions > div:first-child").hasClass("Hidden")) {
        $("span.Left").removeClass("Hide");
      } else {
        $("span.Left").addClass("Hide");
      }

      if ($(".Sessions > div:last-child").hasClass("Hidden")) {
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
            font-family: "Poppins", sans-serif;
            font-size: 26px;
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
      .Card:nth-of-type(1) {
        h3 {
          font-family: "Poppins", sans-serif;
          font-size: 24px;
        }
      }
      .Card:nth-of-type(2) {
        max-width: 500px;
        margin-top: 40px;
        margin-bottom: 40px;
        @include breakpoints(small) {
          max-width: 600px;
        }
        h3 {
          font-family: "Poppins", sans-serif;
          font-size: 24px;
          @include breakpoints(mobile) {
            font-size: 22px;
          }
        }

        p:nth-child(1) {
          color: rgb(86, 86, 87);
          font-size: 19px;
          margin-bottom: 5px;
          @include breakpoints(mobile) {
            font-size: 17px;
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
          padding: 20px 15px;
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
        max-width: 500px;
        h3 {
          font-family: "Poppins", sans-serif;
          font-size: 24px;
          @include breakpoints(mobile) {
            font-size: 20px;
          }
        }
        a {
          color: #6864b9;
          cursor: pointer;
          text-decoration: none;
        }
        .HideRecommend {
          display: none;
        }
        .HideRe {
          display: none;
        }
      }
    }
    .blue-Card {
      background-color: #bddfeb;
      border-radius: 25px;
      width: 100%;
      max-width: 600px;
      margin: auto;
      .StudentCourses {
        h3 {
          font-weight: 600;
          font-size: 25px;
          font-family: "Poppins", sans-serif;
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
