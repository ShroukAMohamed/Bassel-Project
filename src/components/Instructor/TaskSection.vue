<template>
  <div>
    <RateTask />
    <SeeTask />
    <a class="UpArrow"><i class="fa-solid fa-arrow-up"></i></a>
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div
            class="GroupCard d-flex flex-column flex-lg-row align-items-center"
          >
            <div class="col-lg-5 col-12">
              <img
                class="img-fluid"
                src="../../assets/undraw_working_remotely_re_6b3a.svg"
                alt=""
              />
            </div>
            <div class="col-lg-7 col-12 mt-4 mt-lg-0">
              <h3 class="text-center">Group 1 ( Front-End )</h3>
              <GroupsSessions carouselNo="Group1" carouselNoBtn="#Group1" />
            </div>
          </div>
          <div
            class="GroupCard d-flex flex-column flex-lg-row align-items-center mt-5"
          >
            <div class="col-lg-5">
              <img
                class="img-fluid"
                src="../../assets/undraw_working_remotely_re_6b3a.svg"
                alt=""
              />
            </div>
            <div class="col-lg-7 col-12 mt-4 mt-lg-0">
              <h3 class="text-center">Group 2 ( Front-End )</h3>
              <GroupsSessions carouselNo="Group2" carouselNoBtn="#Group2" />
            </div>
          </div>
          <div
            class="GroupCard d-flex flex-column flex-lg-row align-items-center mt-5"
          >
            <div class="col-lg-5">
              <img
                class="img-fluid"
                src="../../assets/undraw_working_remotely_re_6b3a.svg"
                alt=""
              />
            </div>
            <div class="col-lg-7 col-12 mt-4 mt-lg-0">
              <h3 class="text-center">Group 3 ( Front-End )</h3>
              <GroupsSessions carouselNo="Group3" carouselNoBtn="#Group3" />
            </div>
          </div>
        </div>
        <div id="SessionState" class="col-lg-4 gy-5 gy-lg-0 showState">
          <div class="StudentCard pt-4 pb-4 mb-4">
            <h4 class="text-center mb-0 pb-3">
              Session State
              <span class="ms-2 text-success"
                ><i class="fa-solid fa-pen-to-square"></i
              ></span>
            </h4>
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
            <StudentTask />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import StudentTask from "./TaskSection/StudentsTasks.vue";
import GroupsSessions from "./TaskSection/GroupsSessions.vue";
import RateTask from "./TaskSection/RateTask.vue";
import SeeTask from "./TaskSection/SeeTask.vue";
import $ from "jquery";
export default {
  name: "TaskSection",
  components: { GroupsSessions, StudentTask, RateTask, SeeTask },
  mounted() {
    $(".Sessions a").click(function () {
      $(".showState").fadeIn();
    });
    $(".UpArrow").click(function () {
      $(window).scrollTop(0);
    });
    $(window).scroll(function () {
      if ($(this).scrollTop() > 500) {
        $(".UpArrow").fadeIn();
      } else {
        $(".UpArrow").fadeOut();
      }
    });
  },
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.UpArrow {
  position: fixed;
  bottom: 2%;
  right: 2%;
  background-color: rgb(0, 140, 255);
  padding: 10px 15px;
  text-align: center;
  border-radius: 5px;
  color: white;
  cursor: pointer;
  display: none;
}
.GroupCard {
  background-color: white;
  box-shadow: 0px 3px 20px #00000029;
  border-radius: 25px;
  padding-top: 25px;
  padding-bottom: 35px;
  width: 100%;
  @include breakpoints(small) {
    max-width: 550px;
    margin: auto;
  }

  .Hide {
    display: none;
  }
  > div:nth-child(2) {
    span:first-child,
    span:last-child {
      font-size: 28px;
      cursor: pointer;
    }
  }
}

.showState {
  display: none;
  .StudentCard {
    background-color: rgba(217, 204, 204, 0.156);
    box-shadow: 0px 3px 8px #00000029;
    border-radius: 10px;
    width: 100%;
    max-width: 400px;
    margin: auto;
    height: 100%;
    max-height: 1000px;
    overflow: auto;
    @include breakpoints(small) {
      max-width: 550px;
    }
    h4 {
      font-size: 26px;
    }
  }
}
</style>
