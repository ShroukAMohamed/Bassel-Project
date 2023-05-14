<template>
  <div class="Enroll d-flex justify-content-center align-items-center">
    <Navbar />
    <PaymentComponent />
    <VisaMethod />
    <SuccessComponent />
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-12 text-center pb-3 pb-sm-5">
          <h2>{{ CourseName }}</h2>
        </div>
        <div class="col-lg-6 col-12">
          <div class="course-details">
            <div class="course-img">
              <div class="overlay"></div>
              <div class="h-100 d-flex justify-content-center flex-column">
                <div class="d-flex justify-content-between">
                  <div class="download col-5 mt-2 mt-sm-3 ms-3">
                    <span
                      ><i class="fa-solid fa-download pe-1"></i> Download</span
                    >
                  </div>
                  <div
                    class="promo-code col-md-4 col-6 d-flex flex-column justify-content-center align-items-center"
                  >
                    <span class="ms-3">#Promo Code:</span>
                    <span>{{ Promo_Code }}</span>
                  </div>
                </div>
                <div
                  class="d-flex flex-column text-light justify-content-center align-items-center h-100"
                >
                  <div class="text-style">
                    <p>
                      {{ Course_Details }}
                    </p>
                  </div>
                  <div class="options">
                    <span
                      ><i class="fa-solid fa-laptop-code"></i>
                      {{ N_Tracks }} Tracks</span
                    >
                    <span
                      ><i class="fa-solid fa-users"></i>
                      {{ N_Groups }} Group</span
                    >
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-6 col-12">
          <div class="info-card pt-5 pt-sm-3">
            <p>{{ Group_Title }}</p>
            <div class="mb-3">
              <p class="d-inline me-3">{{ CourseState }}</p>
              <span
                >Location:
                <p class="d-inline">{{ CourseLocation }}</p></span
              >
            </div>
            <div class="details mb-3">
              <span
                >From: <span>{{ FromDate }}</span></span
              >
              <span
                >To: <span>{{ ToDate }}</span></span
              >
              <span
                >Duration: <span>{{ Duration }}</span></span
              >
            </div>
            <div class="d-flex justify-content-between">
              <span
                >Max Capacity:
                <p class="d-inline">{{ Max_Capacity }} enrollment</p></span
              >
              <p class="text-danger text-center fw-light mb-0">
                {{ N_Available }} available
              </p>
            </div>
          </div>
          <enrollForm />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/global/Navbar.vue";
import hide_model from "../../mixin/hide_model";
import PaymentComponent from "../components/payment.vue";
import SuccessComponent from "../components/Success.vue";
import VisaMethod from "../components/VisaMethod.vue";
import enrollForm from "../components/Enroll/enrollForm.vue";
export default {
  name: "EnrollPage",
  data() {
    return {
      CourseName: "Course Name Goes Here",
      Promo_Code: "WEDDEV",
      Course_Details:
        "Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi in nibh faucibus, iaculis lorem vitae, cursus velit Mauris imperdiet orci dapibus, commodo libero nec, interdum.",
      N_Tracks: "4",
      N_Groups: "2",
      Group_Title: "Group Title",
      CourseState: "Offline",
      CourseLocation: "Armenia, Cape Town",
      FromDate: "01/30",
      ToDate: "10/30",
      Duration: "10 Days",
      Max_Capacity: "100",
      N_Available: "40",
    };
  },
  components: {
    Navbar,
    PaymentComponent,
    SuccessComponent,
    VisaMethod,
    enrollForm,
  },
  mixins: [hide_model],
  // methods: {
  //  validCard() {
  //    $("#number").formatCardNumber();
  //    $("#expire").formatCardExpiry();
  //    $("#cvv").formatCardCVC();
  //    },
  // },
};
</script>

<style lang="scss" scoped>
@import "../components/global/scss/main.scss";
.Enroll {
  margin: 100px 0;

  .course-details {
    .course-img {
      position: relative;
      background-image: url("../assets/mr-bochelly-IBKyH0V3rew-unsplash@2x.png");
      background-size: cover;
      height: 50vh;
      width: 100%;
      overflow: hidden;
      @include breakpoints(mobile) {
        height: 70vh;
        background-position: 20% 100%;
      }
      .overlay {
        @include overlays;
        background-color: rgba(0, 0, 0, 0.233);
      }
      > div:nth-child(2) {
        z-index: 2;
        position: relative;
        .download {
          span {
            color: white;
            font-weight: 500;
            font-size: 20px;
            @include breakpoints(mobile) {
              font-size: 18px;
            }
          }
        }
        .promo-code {
          background-color: #fbb901;
          color: white;
          clip-path: polygon(25% 0%, 100% 0%, 100% 100%, 25% 100%, 0% 50%);
          @include breakpoints(mobile) {
            font-size: 14px;
          }
          span:last-of-type {
            font-weight: 600;
            letter-spacing: 1px;
          }
        }
        .text-style {
          font-size: 16px;
          width: 90%;
          max-width: 400px;
          text-align: center;
          letter-spacing: 1px;
          font-weight: 400;
          @include breakpoints(mobile) {
            font-size: 14px;
          }
        }
        .options {
          span {
            margin: 0 30px;
            font-size: 17px;
            font-weight: bold;
            @include breakpoints(mobile) {
              font-size: 14px;
            }
          }
        }
      }
    }
  }
  .info-card {
    background-color: #f1f1f1;
    padding: 20px;
    border-radius: 12px;
    position: relative;
    &::before {
      content: "1000 EGP";
      position: absolute;
      right: 0;
      color: white;
      padding: 13px 0;
      padding-left: 35px;
      padding-right: 15px;
      font-weight: 600;
      top: 5%;
      clip-path: polygon(25% 0%, 100% 0%, 100% 100%, 25% 100%, 0% 50%);
      background-color: #ffb12b;
    }
    p {
      font-weight: 500;
      color: #515661;
      font-size: 17px;
      letter-spacing: 1px;
    }
    span:not(.details span) {
      font-weight: 300;
      color: #515661;
      font-size: 18px;
      letter-spacing: 1px;
    }
    .details {
      span {
        font-weight: 300;
        color: #515661;
        font-size: 18px;
        letter-spacing: 1px;
        span {
          font-weight: 500;
          font-size: 17px;
          margin-right: 10px;
        }
      }
    }
  }
}
</style>
