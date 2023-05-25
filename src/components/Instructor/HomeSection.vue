<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-4 col-md-6 gy-1 gy-md-0 order-1 order-md-2">
        <div class="Card text-center">
          <h3>Overall Due Amount</h3>
          <div class="mt-3 d-flex justify-content-center align-items-center">
            <img src="../../assets/4098101_icon.png" alt="" />
            <h4 class="ms-3 mt-2">$544K</h4>
          </div>
        </div>
      </div>
      <div class="col-lg-4 col-md-6 order-2 gy-5 gy-md-0">
        <div class="Card text-center">
          <h3>Assigned Groups</h3>
          <div class="mt-3 d-flex justify-content-center align-items-center">
            <img src="../../assets/group_team_people_icon_48.png" alt="" />
            <p class="ms-3 mt-2 mb-0">5 Groups</p>
          </div>
        </div>
      </div>
      <div class="col-lg-4 col-12 gy-5 gy-lg-0 order-3">
        <div class="Card text-center">
          <h3>Next Session Time</h3>
          <div class="mt-3 d-flex justify-content-center align-items-center">
            <img
              src="../../assets/4757452_clock_date_hour_schedule_time_icon.png"
              alt=""
            />
            <div class="d-flex flex-column ms-3">
              <span>Monday</span>
              <span>12:00 AM</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-lg-6 order-last">
        <Registered
          :Full_Name="full_name"
          :Email="email"
          :PhoneـNumber="phoneـnumber"
          :DetailedـAddress="detailedـaddress"
          :Birth_Date="birth_date"
        />
      </div>
      <div class="col-lg-6 gy-5 mb-4 order-first order-md-last">
        <div class="RateCard ps-sm-4 pe-sm-4">
          <div
            class="d-flex flex-sm-row justify-content-between flex-column align-items-center"
          >
            <h5 class="ms-sm-3 ms-0 fw-bold pb-2 pb-sm-0 text-light">
              Your Ratings
              <i class="fa-regular fa-thumbs-up text-light"></i>
            </h5>
            <p>Average Rate: <span>4.5/5</span></p>
          </div>
          <RateCard />
          <RateCard />
          <RateCard />
          <RateCard />
          <RateCard />
          <RateCard />
          <RateCard />
          <RateCard />
        </div>
      </div>
    </div>
  </div>
  <!--Home Section-->
</template>

<script>
import Registered from "@/components/Registered.vue";
import RateCard from "./HomeSection/RateCards.vue";
export default {
  name: "HomeSection",
  data() {
    return {
      full_name: "Full Name",
      email: "Email",
      phoneـnumber: "Phone Number",
      detailedـaddress: "Detailed Address",
      birth_date: "Date of birth",
    };
  },
  components: { Registered, RateCard },
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.row {
  .Card {
    background-color: rgb(253, 254, 255);
    box-shadow: 0px 3px 20px #00000029;
    padding: 30px 0;
    border-radius: 10px;
    width: 100%;
    max-width: 400px;
    font-family: "Asap", serif;
    @include breakpoints(small) {
      max-width: 500px;
    }
    margin: auto;
    h3 {
      font-size: 29px;
      padding-bottom: 8px;
      color: #292929;
      letter-spacing: 0.5px;
      font-weight: bold;
    }
    h4 {
      font-size: 30px;
      color: rgb(44, 44, 44);
      letter-spacing: 1.5px;
    }
    span {
      font-size: 20px;
      font-weight: 500;
      color: #212121;
    }
    p {
      font-size: 27px;
      font-weight: 500;
    }
  }
  > div:nth-child(2) {
    .Card {
      background: transparent linear-gradient(180deg, #1984ff 40%, #65c1ff) 0%
        0% no-repeat padding-box;
      color: white;
      padding: 38px 0;
      h3 {
        color: white;
      }
    }
  }
  .RateCard {
    background: transparent linear-gradient(90deg, #3288ff 20%, #5ebfff) 0% 0%
      no-repeat padding-box;
    box-shadow: 0px 3px 15px #00000029;
    padding: 36px 5px;
    border-radius: 10px;
    height: 100%;
    max-height: 590px;
    overflow: auto;
    width: 100%;
    max-width: 680px;
    margin: auto;
    font-family: "Asap", serif;

    div {
      h5 {
        font-size: 23px;
        letter-spacing: 0.5px;
      }
      > p {
        font-size: 18px;
        background-color: white;
        padding: 2px 10px;
        border-radius: 5px;
        span {
          color: #ffa200;
        }
      }
    }
  }
}
</style>
