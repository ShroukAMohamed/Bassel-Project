<template>
  <div>
    <Navbar />
    <PaymentComponent />
    <VisaMethod />
    <SuccessComponent />
    <MilePopup />
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
                  class="col-md-5 text-center text-md-start d-flex flex-column justify-content-center"
                >
                  <h3>Your Dashboard</h3>
                  <p class="mt-4 m-auto ms-md-0 text-start">
                    Welcome back, {{ client_name }}
                  </p>
                  <img
                    class="img-fluid mt-4"
                    src="../assets/Mask Group 13@2x.png"
                    alt=""
                  />
                </div>
                <div class="col-md-7 gy-5 gy-md-0">
                  <Completion />
                </div>
              </div>
              <div class="Card mt-4 m-auto me-md-3 me-lg-0">
                <div class="d-flex justify-content-between align-items-center">
                  <div>
                    <h3>{{ salary }}</h3>
                    <p class="mb-0">{{ project_name }}</p>
                  </div>

                  <span
                    data-bs-target="#exampleModal"
                    data-bs-toggle="modal"
                    data-bs-dismiss="modal"
                  >
                    <i class="fa-solid fa-location-arrow"></i>
                  </span>
                </div>
              </div>
              <!-- <Calendar /> -->
            </div>
            <div
              data-aos="fade-left"
              data-aos-duration="1000"
              class="col-lg-6 gy-5 gy-lg-0"
            >
              <div class="blue-Card ps-md-4 pe-md-4 ps-2 pe-2">
                <div
                  class="d-flex flex-column align-items-center flex-xl-row pb-3 justify-content-xl-between courses-board"
                >
                  <h3>
                    Your Projects <span class="ms-1">{{ project_number }}</span>
                  </h3>
                  <div class="mt-4 mt-xl-0">
                    <input type="text" placeholder="Search" />
                  </div>
                </div>
                <ClientProject />
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
  </div>
</template>

<script>
import Navbar from "@/components/global/Navbar.vue";
import PaymentComponent from "../components/payment.vue";
import VisaMethod from "../components/VisaMethod.vue";
import SuccessComponent from "../components/Success.vue";
import ClientProject from "../components/Client/ClientProject.vue";
import MilePopup from "../components/Client/MilePopup.vue";
import RegistInfo from "../components/Registered.vue";
import Completion from "@/components/Client/Completion.vue";
export default {
  name: "ClientBoard",
  data() {
    return {
      client_name: "Jerry Garrett",
      salary: "$223K",
      project_name: "Project Name Due",
      project_number: "2",
      Full_Name: "Full Name",
      Email: "Email",
      PhoneـNumber: "Phone Number",
      DetailedـAddress: "Detailed Address",
      Birth_Date: "Date of birth",
    };
  },
  components: {
    Navbar,
    PaymentComponent,
    VisaMethod,
    SuccessComponent,
    ClientProject,
    MilePopup,
    RegistInfo,
    Completion,
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
      box-shadow: 0px 7px 22px #0000001a;
      padding: 20px;
      width: 100%;
      margin: auto;
      border-radius: 15px;
      margin-right: 0;
    }

    .first-part {
      > div:first-child {
        > div:first-child {
          h3 {
            position: relative;
            font-family: "Poppins", sans-serif;
            font-size: 25px;
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
          p {
            font-size: 20px;
            width: 100%;
            max-width: 150px;
            letter-spacing: 0.5px;
            font-family: "Asap", sans-serif;
          }
        }
      }
      .Card:nth-of-type(2) {
        max-width: 360px;
        margin-bottom: 40px;
        padding: 20px 30px;
        @include breakpoints(small) {
          max-width: 550px;
        }
        h3 {
          font-size: 25px;
          font-weight: bold;
        }
        span {
          background-color: #00ccf2;
          padding: 7px 14px;
          border-radius: 50%;
          color: white;
          font-size: 20px;
          cursor: pointer;
        }
      }
    }
    .blue-Card {
      background-color: #bddfeb;
      padding: 25px 0;
      border-radius: 25px;
      width: 100%;
      max-width: 550px;
      margin: auto;
      position: relative;
      .courses-board {
        h3 {
          font-weight: 600;
          font-size: 26px;
          font-family: "Poppins", sans-serif;
          font-size: 25px;
          span {
            background-color: white;
            color: #2596be;
            border-radius: 50%;
            padding: 3px 11px;
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
            width: 100%;
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
