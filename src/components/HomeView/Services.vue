<template>
  <div>
    <section class="Services block" id="Services">
      <div class="service-img">
        <div class="container">
          <div class="row">
            <div class="col-12 Service-info">
              <h2 class="text-center">SERVICES & NUMBERS</h2>
            </div>
            <div
              data-aos="zoom-in"
              data-aos-duration="1000"
              class="col-md-4 col-12 text-center"
            >
              <div class="Card">
                <div class="pt-4">
                  <img class="pb-4" src="../../assets/MaskGroup2.svg" alt="" />
                  <h4>Web Development</h4>
                  <p class="pt-2">
                    Mauris imperdiet orci dapibus, commodo libero nec, interdum
                    tortor Mauris.
                  </p>
                  <div class="pb-4 mt-4"><a href="#Contact">Contact Us</a></div>
                </div>
              </div>
            </div>
            <div
              data-aos="zoom-in"
              data-aos-duration="1000"
              class="col-md-4 col-12 gy-5 gy-md-0 text-center"
            >
              <div class="Card">
                <div class="pt-4">
                  <img class="pb-4" src="../../assets/MaskGroup2.svg" alt="" />
                  <h4>Web Development</h4>
                  <p class="pt-2">
                    Mauris imperdiet orci dapibus, commodo libero nec, interdum
                    tortor Mauris.
                  </p>
                  <div class="pb-4 mt-4"><a href="#Contact">Contact Us</a></div>
                </div>
              </div>
            </div>
            <div
              data-aos="zoom-in"
              data-aos-duration="1000"
              class="col-md-4 col-12 gy-5 gy-md-0 text-center"
            >
              <div class="Card">
                <div class="pt-4">
                  <img class="pb-4" src="../../assets/MaskGroup3.svg" alt="" />
                  <h4>Web Development</h4>
                  <p class="pt-2">
                    Mauris imperdiet orci dapibus, commodo libero nec, interdum
                    tortor Mauris.
                  </p>
                  <div class="pb-4 mt-4"><a href="#Contact">Contact Us</a></div>
                </div>
              </div>
            </div>
          </div>
          <div class="row justify-content-center serviceNum">
            <div
              data-aos="fade-in"
              data-aos-duration="600"
              class="col-lg-3 col-md-6 col-12 gy-4 text-center"
            >
              <div
                class="circle circle-1 d-flex justify-content-center align-items-center"
              >
                <img class="pe-lg-3" src="../../assets/Group284.svg" alt="" />
              </div>
              <p class="pt-3">Successful Projects</p>
            </div>
            <div
              data-aos="fade-in"
              data-aos-duration="600"
              data-aos-delay="200"
              class="col-lg-3 col-md-6 col-12 pt-5 pt-lg-0 gy-4 text-center"
            >
              <div
                class="circle circle-2 d-flex justify-content-center align-items-center"
              >
                <img class="" src="../../assets/Group283.svg" alt="" />
              </div>
              <p class="pt-3">Cup Of Coffee</p>
            </div>
            <div
              data-aos="fade-in"
              data-aos-duration="600"
              data-aos-delay="400"
              class="col-lg-3 col-md-6 col-12 text-center pt-5 gy-4 pt-lg-0"
            >
              <div
                class="circle circle-3 d-flex justify-content-center align-items-center"
              >
                <img class="" src="../../assets/MaskGroup5.svg" alt="" />
              </div>
              <p class="pt-3">Students</p>
            </div>
            <div
              data-aos="fade-in"
              data-aos-duration="600"
              data-aos-delay="600"
              class="col-lg-3 col-md-6 col-12 text-center pt-5 gy-4 pt-lg-0"
            >
              <div
                class="circle circle-4 d-flex justify-content-center align-items-center"
              >
                <img class="" src="../../assets/MaskGroup6.svg" alt="" />
              </div>
              <p class="pt-3">Happy Clients</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "ServicesComponent",
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
.Services {
  margin: 50px 0;
  .service-img {
    background-image: url("../../assets/Group281.svg");
    height: 100%;
    background-repeat: no-repeat;
    background-size: cover;
    .Service-info {
      margin-bottom: 80px;
      @include breakpoints(mobile) {
        margin-bottom: 50px;
      }
      h2 {
        font-size: 40px;
        font-weight: bold;
        letter-spacing: 1px;
        font-family: "Poppins", sans-serif;
        @include breakpoints(mobile) {
          font-size: 35px;
        }
      }
    }
    .Card {
      background-color: white;
      box-shadow: 0 0.5rem 3rem rgba(0, 0, 0, 0.15) !important;
      width: 100%;
      max-width: 300px;
      margin: auto;
      border-radius: 10px;
      h4 {
        font-size: 18px;
      }
      p {
        width: 95%;
        max-width: 250px;
        margin: auto;
      }
      a {
        background-color: transparent;
        border: 0;
        color: #6864b9;
        font-weight: 600;
        font-size: 18px;
        text-decoration: underline;
        cursor: pointer;
      }
    }
    .serviceNum {
      margin-top: 120px;
      .circle {
        position: relative;
        border: 1px solid #ffb12b;
        width: 150px;
        height: 150px;
        border-radius: 50%;
        margin: auto;
      }
      .circle {
        &::before {
          content: "+13";
          padding-top: 8px;
          font-size: 20px;
          color: white;
          top: -20%;
          position: absolute;
          width: 55px;
          height: 46px;
          border-radius: 20px;
          background-color: #ffb12b;
        }
      }
      p {
        font-size: 20px;
      }
    }
  }
}
</style>
